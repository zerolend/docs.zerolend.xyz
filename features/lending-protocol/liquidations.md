# Liquidations

The health of the ZeroLend Protocol is dependent on the 'health' of the collateralized positions within the protocol, also known as the 'health factor.' When the 'health factor' of an account's total loans is below 1, anyone can make a `liquidationCall()` to the `Pool` contract, pay back part of the debt owed, and receive discounted collateral in return (also known as the liquidation bonus).

This incentivizes third parties to participate in the health of the overall protocol by acting in their own interest (to receive the discounted collateral) and as a result, ensure borrowers are sufficiently collateralized.

There are multiple ways to participate in liquidations:

1. By calling the `liquidationCall()` directly in the Pool contract.
2. By creating your own automated bot or system to liquidate loans.

For liquidation calls to be profitable, you must take into account the gas cost involved in liquidating the loan. If a high gas price is used, liquidation may be unprofitable for you. See the [Calculating profitability section](liquidations.md#calculating-profitability-vs-gas-cost) for more details.&#x20;

100% of the debt (i.e. `MAX_LIQUIDATION_CLOSE_FACTOR`) can be liquidated in single `liquidationCall()` if: `HF < CLOSE_FACTOR_HF_THRESHOLD`

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

When making a `liquidationCall()`, you must:

* Know the account (i.e., the Ethereum address: `user`) whose health factor is below 1.
* Know the valid debt amount and asset (i.e. `debtToCover` & `debtAsset`)
  * If the HF is above `CLOSE_FACTOR_HF_THRESHOLD`, then only a maximum of 50% (i.e. `DEFAULT_LIQUIDATION_CLOSE_FACTOR`) of the debt can be liquidated per valid `liquidationCall()`
  * If the HF is below `CLOSE_FACTOR_HF_THRESHOLD`, then 100% (i.e. `MAX_LIQUIDATION_CLOSE_FACTOR`) of the debt can be liquidated in a single valid `liquidationCall()`
  * You can set the `debtToCover` to `uint(-1)` and the protocol will proceed with the highest possible liquidation allowed by the close factor.
  * You must already have a sufficient balance of the debt asset, which will be used by the `liquidationCall` to pay back the debt. You can use `flashLoan` for liquidations 😉
* Know the collateral asset `collateralAsset` you closing, i.e., the asset that the user has `backing` their outstanding loan that you will receive as a `bonus`.
* Whether you want to receive _aTokens_ or the underlying asset after a successful `liquidationCall()` .

### Getting accounts to liquidate <a href="#getting-accounts-to-liquidate" id="getting-accounts-to-liquidate"></a>

"User Account" in the ZeroLend Protocol refers to a single Ethereum address interacting with the protocol. This can be an externally owned account or contract.&#x20;

Only user accounts that have HF < 1 can be liquidated. There are multiple ways you can get the health factor:

#### On Chain <a href="#on-chain" id="on-chain"></a>

1.  To gather user account data from on-chain data, one way would be to monitor emitted events from the protocol and keep an up-to-date index of user data locally.

    a. Events are emitted each time a user interacts with the protocol (supply, borrow, repay, withdraw, etc.)
2. When you have the user's address, you can simply call `getUserAccountData()`, to read the user's current healthFactor. If the HF < 1, then the account can be liquidated.

#### GraphQL <a href="#graphql" id="graphql"></a>

1. Similarly to the sections above, you will need to gather user account data and keep an index of the user data locally.
2. Since GraphQL does not provide real-time calculated user data such as `healthFactor,` you will need to compute this locally. The easiest way is to use the ZeroLend-utilities SDK, which has methods to compute user summary data.

### Executing the liquidation call <a href="#executing-the-liquidation-call" id="executing-the-liquidation-call"></a>

Once you have the account(s) to liquidate, you will need to calculate the amount of collateral that can be liquidated:

1. Use `getUserReserveData()`​
2. Max debt that is cleared by a single liquidation call is given by the `DEFAULT_LIQUIDATION_CLOSE_FACTOR`(when `CLOSE_FACTOR_HF_THRESHOLD < HF < 1`) or `MAX_LIQUIDATION_CLOSE_FACTOR` (when `HF < CLOSE_FACTOR_HF_THRESHOLD`)
   1. `debtToCover = (userStableDebt + userVariableDebt) * LiquidationCloseFactor`
   2. You can pass `uint(-1)`, i.e. `MAX_UINT`, as the `debtToCover` to liquidate the maximum amount allowed.
3. Max amount of collateral that can be liquidated to cover debt is given by the current _liquidationBonus_ for the reserves that have `usageAsCollateralEnabled` as true.
   1. `maxAmountOfCollateralToLiquidate = (debtAssetPrice * debtToCover * liquidationBonus)/ collateralPrice`

### Calculating profitability vs. gas cost <a href="#calculating-profitability-vs-gas-cost" id="calculating-profitability-vs-gas-cost"></a>

One way to calculate the profitability is the following:

1. Store and retrieve each collateral's relevant details, such as an address, decimals used, and liquidation bonus.
2. Get the user's collateral balance (aTokenBalance).
3. Get the asset's price according to ZeroLend's oracle contract using `getAssetPrice()`.
4. The maximum collateral bonus received on liquidation is given by the `maxAmountOfCollateralToLiquidate * (1 - liquidationBonus) * collateralAssetPriceEth`
5. The maximum cost of your transaction will be your gas price multiplied by the amount of gas used. You should be able to get a good estimation of the gas amount used by calling `estimateGas` via your web3 provider.
6. Your approximate profit will be the value of the collateral bonus (4) minus the cost of your transaction (5).

## FAQs

### How is the liquidation bonus determined? <a href="#how-is-liquidation-bonus-determined" id="how-is-liquidation-bonus-determined"></a>

Liquidation bonuses for all the assets are evaluated and determined based on each asset's liquidity risk and updated via the Governance process.

### How much is the liquidation penalty?

The liquidation penalty (or bonus for liquidators) depends on the asset used as collateral. You can find every assets' liquidation fee in the [risk parameters section](broken-reference).

### Can you give me an example of a liquidation?

A couple of them here:

**Example 1**&#x20;

1. Bob deposits 10 ETH and borrows 5 ETH worth of DAI.&#x20;
2. If Bob’s Health Factor drops below 1, his loan will be eligible for liquidation.&#x20;
3. A liquidator can repay up to 50% of a single borrowed amount = 2.5 ETH worth of DAI.&#x20;
4. In return, the liquidator can claim a single collateral, ETH (5% bonus). &#x20;
5. The liquidator claims 2.5 + 0.125 ETH for repaying 2.5 ETH worth of DAI.

**Example 2**&#x20;

1. Bob deposits 5 ETH and 4 ETH worth of YFI and borrows 5 ETH worth of DAI&#x20;
2. If Bob’s Health Factor drops below 1, his loan will be eligible for liquidation.&#x20;
3. A liquidator can repay up to 50% of a single borrowed amount = 2.5 ETH worth of DAI.&#x20;
4. In return, the liquidator can claim a single collateral, as the liquidation bonus is higher for YFI (15%) than ETH (5%) if the liquidator chooses to claim YFI. &#x20;
5. The liquidator claims 2.5 + 0.375 ETH worth of YFI for repaying 2.5 ETH worth of DAI.

### How can I avoid getting liquidated?

To avoid liquidation, you can raise your health factor by depositing more collateral assets or repaying part of your loan. By default, repayments increase your health factor more than deposits. Also, it's important to monitor your health factor and keep it high to avoid liquidation. For example, keeping your health factor over 2 gives you more of a margin to avoid liquidation.  \
\
You should be mindful of the stablecoin price fluctuations due to market conditions and how they might affect your health factor. For example, the market price of USDC 1.00 might not equal exactly USD 1.00, but for example, USD 0.95. The price fluctuations of stablecoins, like any assets, affect your health factor.
