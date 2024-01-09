---
description: This page talks about Credit Delegation
---

# Credit Delegation

Credit Delegation is a feature that allows a depositor to deposit funds into ZeroLend for interest earnings while delegating borrowing power (credit) to other users. The loan terms are agreed upon between the depositor and borrowers on-chain via smart contracts. This facilitates extra yield for the depositor and provides uncollateralized loan access for borrowers.

#### **Key Points related to Credit Delegation:**&#x20;

* Depositors (delegators) earn additional yield on top of the protocol's standard yield.
* Borrowers (delegatees) gain access to uncollateralized loans.
* The borrower must align with the depositor's eMode category. Example: If a depositor's eMode category is STABLECOINS, then the delegatee can only borrow assets in the STABLECOINS eMode category. Borrowing outside this category, like in WETH, would result in a failed borrow.
* Delegatees cannot exploit credit approval to liquidate the delegator.
* If a borrow puts the delegator's position below the liquidation threshold, the borrow will fail.

Example: Suppose Alice deposits stablecoins into the protocol, delegates borrowing power to Bob, and agrees that Bob can borrow up to 100 stablecoins. Alice approve this credit. Later, Bob access Alice's available credit. If Bob tries to borrow in a non-stablecoin category, the transaction fails.
