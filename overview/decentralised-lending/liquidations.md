---
description: >-
  ZeroLend has a liquidation mechanism to mitigate the risk of default and
  protect lenders’ capital.
---

# Liquidations

Liquidations are one of the fundamental risks in DeFi lending protocols. Liquidation is the process that occurs when a borrower's [health factor](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/decentralised-lending/getting-started/borrowing#health-factor) goes below 1 due to their collateral value not properly covering their loan/debt position.  \
\
The exact amount of collateral that will be sold to cover the debt depends on several factors, including the liquidation threshold, the liquidation penalty, and the current value of the collateral and the debt.

## How does liquidation work in ZeroLend?

Let's take your example where you have borrowed $10,000 worth of stablecoin against $18,000 worth of ETH as collateral. Assuming a liquidation threshold of 0.8, liquidation is triggered once your health factor hits this level. ZeroLend’s smart contract automatically sells enough collateral to cover the debt, often including a liquidation penalty.

* **Without considering a liquidation penalty**: If we assume that exactly enough collateral is sold to bring your health factor back to 1, liquidators would need to cover a debt of $10,000. Since the health factor is 0.8, it means that your $18,000 collateral is now only worth $12,500 (because $10,000 is 80% of $12,500).&#x20;
* **Considering a liquidation penalty (e.g., 5%)**: ZeroLend liquidators would sell more than the $10,000 debt due to the liquidation penalty. For example, if the penalty is 5% of the amount to be liquidated, we would sell $10,000 + 5% of $10,000 ($500) = $10,500 worth of your collateral.

## Understanding metrics that can lead to liquidation in ZeroLend.&#x20;

It is important to understand how your loan's health factor can drop below 1. Here are a few instances that might lead to liquidation of your funds:&#x20;

1. If you borrow funds against volatile assets, the price of those assets might fluctuate exponentially, leading to liquidation. However, ZeroLend mitigates this risk to some extent by listing volatile assets under [Isolation Mode](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/decentralised-lending/capital-efficiency/isolation-mode).&#x20;
2. The collateral asset provided decreases in value.&#x20;
3. The borrowed debt increases in value against the collateral provided.&#x20;
4. The user fails to meet their interest payments.&#x20;

## Liquidators

Liquidators are advanced DeFi users who have developed automated systems (i.e., bots) to monitor collateralized positions and seek out loans that are eligible for liquidation. These bots then interact with ZeroLend's L2Pool contract and initiate a `liquidationCall().`

This enables Liquidators to pay back part of the debt owed and receive discounted collateral in return (also known as the liquidation bonus). Suppose the total liquidation penalty is 5%. Half of the penalty (2.5%) is allocated as a bonus to liquidators.

This liquidation mechanism incentivizes third parties to participate in the health of the overall protocol by acting in their own interest (to receive the discounted collateral) and, as a result, ensuring that borrows are sufficiently collateralized across the protocol.

### Liquidation Penalty & Risk Parameters&#x20;

Each asset within ZeroLend has different liquidation parameters:

<table><thead><tr><th width="160">Asset </th><th width="125">Max LTV</th><th width="200">Liquidation Threshold</th><th>Liquidation Penalty</th></tr></thead><tbody><tr><td>DAI</td><td>75%</td><td>80%</td><td>5%</td></tr><tr><td>LUSD</td><td>75%</td><td>80%</td><td>5%</td></tr><tr><td>USDC</td><td>80%</td><td>85%</td><td>5%</td></tr><tr><td>USDT</td><td>75%</td><td>80%</td><td>5%</td></tr><tr><td>MUTE</td><td>60%</td><td>90%</td><td>10%</td></tr><tr><td>WBTC</td><td>70%</td><td>75%</td><td>10%</td></tr><tr><td>ETH</td><td>80%</td><td>82.5%</td><td>5%</td></tr></tbody></table>

## How do I avoid liquidation?

In order to avoid the reduction of your health factor leading to liquidation, you can repay the loan or deposit more assets to increase your health factor. Out of these two available options, repaying the loan would improve your health significantly.
