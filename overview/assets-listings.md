# Assets Listings

## Asset Listing Criteria

In a lending platform like ZeroLend, deposited collateral can be considered assets, as one can sell it to recover the loan amount. On the other hand, borrowed amounts are liabilities, as it is an obligation to repay the lender. Asset and liability tokens often differ, with borrowed tokens typically in stablecoins and collateral tokens being volatile.&#x20;

Conducting a thorough analysis before listing a token on ZeroLend is important to reduce market risks.&#x20;

ZeroLend considers a comprehensive set of criteria to evaluate the suitability of adding an asset to the lending pool, like:

* Evaluating the liquidity of the asset to ensure sufficient market depth.
* Conducting a thorough security audit to identify potential risks associated with the token's smart contract.
* Determining the appropriate collateralization ratio for the token to balance risk and ensure the safety of the lending pool.
* Supporting assets with the best risk profiles as collateral.
* Assets with oracles that can be easily manipulated are listed as single-borrow assets.
* Examining the level of community support and engagement for the token.
* New, volatile assets with lower liquidity are considered for listing in [Isolation mode](../features/capital-efficiency/isolation-mode.md) to enable supplying/borrowing for such assets.&#x20;

{% hint style="info" %}
Want us to list your favorite assets? Share your suggestions on ZeroLend’s [Discord](https://discord.gg/zerolend) server.&#x20;
{% endhint %}

## Supported Assets

<figure><img src="../.gitbook/assets/ZL Doc - Supported Assets.png" alt=""><figcaption></figcaption></figure>

### Blue Chips:

* Assets with a market capitalization exceeding $100 million and a liquidity of at least $100 million are included in this category.&#x20;
* Examples:  $ETH, $WBTC, etc.&#x20;

### Stablecoins:&#x20;

* The stablecoins category includes crypto tokens backed by the value of US dollars in a 1:1 ratio.&#x20;
* Examples: $USDT, $USDC, $DAI, etc.&#x20;

### Yield Bearing:

* These assets contribute to yield-bearing strategies, enhancing the earning potential within the ZeroLend ecosystem.&#x20;
* Examples: $ezETH, $rsETH, $weETH, $pufETH, etc.&#x20;

### High Risk:

* This category encompasses assets that do not fit into the Blue Chips criteria. High-risk assets offer an opportunity for diversification but come with increased risk.&#x20;
* Examples: $GRAI, $MUTE, etc.&#x20;
