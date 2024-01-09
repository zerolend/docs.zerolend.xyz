---
description: This page is a comprehensive guide to borrowing on ZeroLend.
---

# Borrowing

Before engaging in the borrowing process, it is essential to ensure that you have appropriately deposited assets as collateral (refer to the [Lending](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/decentralised-lending/getting-started/lending) section for detailed information).

After successfully depositing assets as collateral:\
1\. Proceed to the dashboard page and select the desired assets for borrowing. \
2\. Specify the desired borrowing amount.\
3\. Click "**Confirm**" and authorize the transaction through the provided pop-up wallet prompt.

{% hint style="info" %}
Note: Opting to borrow larger amounts will have a proportional impact on your overall Health Factor (further details are provided below).
{% endhint %}

## Borrowing Eligibility

The maximum borrowing limit for users is determined by factors such as deposit value, asset type, and the liquidity of the deposited assets. The assets supplied by users directly influence the maximum allowable loan value. Additionally, borrowing limits are constrained by the health factor, meaning borrowing an asset becomes restricted if the Health Factor is too low.

The maximum amount you can borrow against your collateral's value is the maximum **Loan-to-Value (LTV)** ratio. If you exceed this level, your collateral will start being sold to cover the debt. For example, with a max LTV of 80%, users can borrow up to 80% of their collateral's assessed value. To illustrate, if the collateral is valued at $100, the user can borrow up to $80.

## Borrowing interest

Borrowing through ZeroLend incurs specific fees, which vary for each asset that ZeroLend supports. There are two types of Annual Percentage Rates (APY) – variable APY, subject to market conditions and recommended for short-term positions, and stable APY, which remains constant throughout the loan period and is ideal for prolonged durations and users seeking predictability.

## Health Factor

Health Factor is a metric used to assess the safety of a loan in terms of its collateralization. ZeroLend's Health Factor closely aligns with the metrics users would encounter in other money markets like Aave to provide users with insight into their proximity to potential liquidation.

* **Safe Zone**: Generally, a health factor above 1 indicates that the loan is currently safe from liquidation. The higher the number, the safer the loan. It means the value of the collateral is sufficiently above the amount borrowed.
* **Risk of Liquidation**: If the health factor drops to 1 or below, the loan is at risk of liquidation. This means ZeroLend can sell the collateral to pay back the loan at a penalty fee of 5%.

## How do I repay my loan?

You repay the loan with the same asset you borrowed. For example, if you initially borrow 2 $ETH, you need to pay back 2 $ETH plus the accrued interest. Repayment can only be made with your wallet balance and not collateral.

Follow these steps:

1. Visit the dashboard and click on the asset for which you wish to repay the debts.
2. Enter the amount you want to repay; the tokens will be deducted from your wallet balance.
3. Click on the "**Confirm**" button and approve the transaction in your wallet.

Once the transaction is successful, the loan is repaid at the specified amount.
