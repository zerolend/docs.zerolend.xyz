---
description: This page talks about Credit Delegation
---

# Credit Delegation

Credit delegation allows a depositor to deposit funds in the protocol to earn interest and delegate borrowing power (i.e., their credit) to other users. The loan enforcement and its terms are agreed upon between the depositor and borrowers, either off-chain via legal agreements or on-chain via smart contracts. This enables:

* The supplier (aka delegator) to earn an extra yield on top of the yield they already earn from the protocol,
* The borrowers (aka delegatees) access an un-collateralized loan.

Borrow by _delegatee_ must be consistent with the _delegator_ [E-Mode ](https://docs.mahalend.com/protocol/high-efficiency-mode)category. For e.g., if a delegator E-Modecategory is `STABLECOINS`, then

* delegator can only borrow `STABLECOINS` E-Mode category asset.
* in case the _delegator_ approves credit to the _delegatee_ for non `STABLECOINS`category (for e.g., wETH), then borrow would revert.

The _delegatee_ cannot abuse credit approval to liquidate the _delegator,_ i.e., if the borrow puts the _delegator's_ position in HF < `HEALTH_FACTOR_LIQUIDATION_THRESHOLD`, then borrow will fail.

### Approving the delegation <a href="#approving-the-delegation" id="approving-the-delegation"></a>

The `approveDelegation()` or `delegationWithSig()` must be called by the supplier (delegator), approving the borrower (delegatee) a certain amount. This is done for each debt token that needs to be delegated. The delegator does not need to already have supplied funds in the protocol to `approveDelegation()`. However, **before** the delegatee executes, there must be sufficient collateral supplied by the delegator in the protocol.

### Borrowing the credit <a href="#borrowing-the-credit" id="borrowing-the-credit"></a>

The borrower (delegatee) calls the `borrow()` method on the `Pool`, using the supplier's (delegator's) address in the final parameter `onBehalfOf`.The borrower's available credit is reduced by the borrowed amount.

### Repaying the credit <a href="#repaying-the-credit" id="repaying-the-credit"></a>

Anyone can repay the debt _OnBehalf_ of the user by calling one of the methods - `repay()` or `repayWithPermit()`. The supplier (aka creditor) can also use `repayWithATokens()` method to repay debt with their _aTokens_ of the underlying debt asset in the same pool.
