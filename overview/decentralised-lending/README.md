---
description: This page talks in detail about the lending protocol of ZeroLend.
---

# Decentralised Lending

ZeroLend's core product is its decentralized non-custodial liquidity market. ZeroLend is a fork of [AAVE V3](https://aave.com/) with changes in the incentive mechanisms that make it very similar to [Radiant Capital](https://radiant.capital/).

## How does lending work in TradFi?

Lending in DeFi differs significantly from TradFi in several key aspects. In traditional banking, obtaining a loan involves a rigorous process of credit score assessment, collateral requirements, and often limited accessibility. Banks act as intermediaries, collecting deposits from lenders and lending out funds to borrowers at a higher interest rate.

Supplier interest < Borrower interest, generating profit from the interest rate spread.

In TradFi, undercollateralized loans are common, where the collateral factor typically exceeds 100%. For instance, with a collateral factor of 300%, a $100 collateral deposit could enable borrowing up to $300.

## How is ZeroLend different from TradFi lending?

ZeroLend introduces a permissionless lending system, meaning that the protocol's services are entirely open to anyone, regardless of their financial or geographical background.  For instance, you can borrow $ETH with a collateral factor of 85%, meaning you can borrow up to 0.85ETH with a 1ETH collateral deposit.

### Why will users borrow if we provide only undercollateralised loans?

Let’s understand this with an example. Let's say you're bullish on $ETH. Instead of idly holding $ETH in your wallet, you can deposit your ETH as collateral on ZeroLend and borrow $USDT to buy other tokens you're bullish on. Win-Win.

## The Basics of ZeroLend

* **Lend** tokens and **earn** lending interest.
* **Borrow** tokens and **pay** borrowing interest.
* In case of **liquidation**, pay a 5% **penalty fee.**

## The Advanced Features of ZeroLend

Many features make ZeroLend attractive to use. The following list below summarises each of them.

* [High Efficiency Mode](../../capital-efficiency/high-efficiency-mode-e-mode.md)
* [Isolation Mode](../../capital-efficiency/isolation-mode.md)
* [Credit Delegation](../../capital-efficiency/credit-delegation.md)

### Important parameters

There are a few parameters that are important in the context of lending:

1. **Max LTV (Loan to Value)**: This is the maximum ratio of the loan amount to the value of the collateral. For instance, a max LTV of 80% means you can borrow up to 80% of your collateral's value. If your collateral is worth $100, you can borrow up to $80.
2. **Liquidation Threshold**: This is the value at which your loan becomes undercollateralized and is at risk of liquidation. For instance, if the threshold is set at 82.50%, and the value of your collateral falls to this percentage of your loan amount, the collateral can be sold off by the protocol to pay back part of the loan.
3. **Liquidation Penalty**: If your loan is liquidated due to falling below the liquidation threshold, this penalty is added to your debt as an extra cost. ZeroLend applied a 5% liquidation fee, meaning that if you're liquidated, you'll pay an additional 5% of the loan value.
4. **Utilization Rate**: This is the percentage of funds that are currently being borrowed compared to the total funds available for borrowing. A utilization rate of 27.20% means that out of all the funds available to be lent out, 27.20% are currently taken by borrowers. This rate can affect the interest rates charged on the loans – generally, the higher the utilization rate, the higher the interest rates, as the demand for the funds is higher relative to the supply.
5. **Health Factor**: This is an indicator of the safety of your loan relative to your collateral. A health factor above 1 means you are not at immediate risk of liquidation. If the health factor falls below 1, it means the loan is undercollateralized and may be liquidated.
