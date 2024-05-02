---
description: >-
  This page explains liquidations, its pros, cons, and how liquidations are
  executed on ZeroLend.
---

# Liquidations

ZeroLend has a liquidation mechanism to mitigate the risk of default and protect lenders’ capital.

Liquidation is the process of selling borrowers’ deposited collateral to repay the debt if the health factor of their acquired loan goes below 1. As one of the major risks in DeFi lending, borrowers must constantly monitor their loans and adjust the collateral or repay the loan based on the health factor to avoid liquidation.

The amount of collateral to be sold is determined by several factors, including the liquidation threshold, liquidation penalty, the current value of the collateral, and the debt amount.&#x20;

### Monitoring Loan Health

ZeroLend tracks loan health using two pivotal metrics: the Loan-to-Value (LTV) ratio and the liquidation threshold.&#x20;

The LTV ratio defines the maximum borrowing capacity against specific collateral. The liquidation threshold marks the point at which a loan is considered under-collateralized and at risk of liquidation.

### How does liquidation work on ZeroLend?

<figure><img src="../../.gitbook/assets/ZL Doc - How liquidation works.png" alt=""><figcaption></figcaption></figure>

On ZeroLend, loan stability and solvency are continuously monitored through a metric called the ‘Health Factor.’&#x20;

The health factor compares a user's collateral against their borrowed amount. Maintaining a Health Factor above 1 is essential for the loan's safety. ZeroLend sells enough collateral to bring the health factor back to permitted levels if it falls below this threshold.&#x20;

The ZeroLend protocol defines two thresholds for liquidation:

1. 50% liquidation occurs when the health factor dips below 1.&#x20;
2. 100% liquidation occurs if the health factor falls below a dynamically determined lower threshold.

For example, you borrowed $10,000 worth of stablecoins against $18,000 worth of $ETH as collateral. Assume the liquidation threshold of your loan is 0.8. If your loan's health factor hits this threshold, ZeroLend’s smart contract automatically sells enough collateral to cover the debt, often including a liquidation penalty.

**Without considering a liquidation penalty:** If we assume that exactly enough collateral is sold to bring your health factor back to 1, liquidators would need to cover a debt of $10,000. Since the health factor is 0.8, your $18,000 collateral is now only worth $12,500.&#x20;

**Considering a liquidation penalty (e.g., 5%):** ZeroLend would sell more than the $10,000 debt due to the liquidation penalty. For example, if the penalty is 5% of the amount to be liquidated, we would sell $10,000 + 5% of $10,000 ($500), i.e., $10,500 worth of your collateral.

### When will your collateral be liquidated on ZeroLend?&#x20;

To avoid liquidation, it is important to understand how your loan's health factor can drop below 1. Here are a few instances that might lead to liquidation:

1. If you borrow funds against volatile assets, the price of those assets might fluctuate exponentially, leading to liquidation. However, ZeroLend helps you mitigate this risk to some extent by listing volatile assets under[ Isolation Mode](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/decentralised-lending/capital-efficiency/isolation-mode).
2. Your deposited collateral asset decreases in value.
3. The borrowed debt increases in value against the deposited collateral.&#x20;
4. The user fails to meet their interest payments.

### Liquidators

Liquidators are advanced DeFi users with automated systems (i.e., bots) to monitor collateralized positions and seek out loans that are eligible for liquidation. These bots then interact with ZeroLend's L2Pool contract and initiate a `liquidationCall().`&#x20;

This enables Liquidators to pay back part of the debt owed and receive discounted collateral in return (also known as the liquidation bonus). Suppose the total liquidation penalty is 5%. Half of the penalty (2.5%) is allocated as a bonus to liquidators.

Such a liquidation mechanism incentivizes third parties to participate in the health of the overall protocol by acting in their own interest (to receive the discounted collateral). Liquidators ensure borrows are sufficiently collateralized across the protocol.

### Liquidation Bonuses and Risks

The incentive for executing a liquidation, known as the liquidation bonus, varies with the collateral's risk profile.&#x20;

Higher-risk collateral results in more significant bonuses for the liquidator, encouraging proactive identification and resolution of risky loans. ZeroLend closely monitors market trends to offer competitive liquidation bonuses to strengthen the protocol's risk management framework.

### Liquidation Mechanics

To initiate a liquidation on ZeroLend, the following inputs are required:

* User's Wallet Address: Must have a Health Factor below 1.
* Debt Coverage Amount: The amount of debt the liquidator intends to cover.
* Debt Asset: Must have a sufficient quantity of the asset, with flash loans playing a crucial role.
* Collateral Asset: Initially provided by the user.
* Profit Asset: Chosen by the liquidator, either in Zerolend's native tokens or the underlying asset.

### Executing a Liquidation

Liquidation is a multistep process that can be automated using bots.&#x20;

It involves:&#x20;

* Verifying the user's low health factor.
* Assessing the profitability of the liquidation, considering transaction fees and bonuses.
* Utilizing flash loans if needed.
* Executing necessary collateral swaps.
* Completing the liquidation process.

### Liquidation Penalty & Risk Parameters&#x20;

Each supported asset on ZeroLend has different liquidation parameters:

### Liquidation Penalty & Risk Parameters&#x20;

Each asset within ZeroLend has different liquidation parameters:

<table><thead><tr><th width="170">Asset </th><th width="125">Max LTV</th><th width="200">Liquidation Threshold</th><th>Liquidation Penalty</th></tr></thead><tbody><tr><td>DAI</td><td>75%</td><td>80%</td><td>5%</td></tr><tr><td>LUSD</td><td>75%</td><td>80%</td><td>5%</td></tr><tr><td>USDC</td><td>80%</td><td>85%</td><td>5%</td></tr><tr><td>USDT</td><td>75%</td><td>80%</td><td>5%</td></tr><tr><td>MUTE</td><td>60%</td><td>90%</td><td>10%</td></tr><tr><td>WBTC</td><td>70%</td><td>75%</td><td>10%</td></tr><tr><td>ETH</td><td>80%</td><td>82.5%</td><td>5%</td></tr></tbody></table>

### How do I avoid liquidation?

To avoid liquidation, you should improve the health factor of your borrowed loan by repaying it or depositing more assets. Out of these two available options, repaying the loan would improve your health significantly.
