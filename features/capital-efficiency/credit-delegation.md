---
description: This page discusses ZeroLend’s credit delegation feature.
hidden: true
---

# Credit Delegation

Credit Delegation is a feature that allows a depositor to deposit funds into ZeroLend to earn interest while delegating borrowing power (credit) to other users. The loan terms are agreed upon between the depositor and borrowers on-chain via smart contracts. This feature facilitates extra yield for the depositor and provides uncollateralized loan access for borrowers.

## Key points to remember while using credit delegation on ZeroLend&#x20;

* Depositors (delegators) earn additional yield on top of the protocol's standard yield.
* Borrowers (delegatees) gain access to uncollateralized loans.
* The borrower must align with the depositor's eMode category.&#x20;

Example: If a depositor's eMode category is STABLECOINS, then the delegatee can only borrow assets in that category. Borrowing outside this category, like $wETH, would result in a failed transaction.&#x20;

* Delegatees cannot exploit credit approval to liquidate the delegator.
* The loan will not be processed if a borrow puts the delegator's position below the liquidation threshold.&#x20;

<figure><img src="../../.gitbook/assets/ZL Doc - Credit Delegation.png" alt=""><figcaption></figcaption></figure>

Example: Suppose Alice deposits stablecoins into the protocol, delegates borrowing power to Bob, and agrees that Bob can borrow up to 100 stablecoins. Alice approved this credit. Later, Bob accessed Alice's available credit. If Bob tries to borrow in a non-stablecoin category, the transaction fails.\
