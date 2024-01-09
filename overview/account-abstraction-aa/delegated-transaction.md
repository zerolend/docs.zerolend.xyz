---
description: This page talks about how the delegated transactions work
---

# Delegated transaction

Collateral monitoring is a challenge in the lending ecosystem in DeFi. Managing collateral and loans on platforms such as Compound requires continuous monitoring and adjustments to prevent losses because if the price of your collateral token drops and your collateral gets liquidated. This process can be demanding and stressful for users.

ZeroLend's integration of account abstraction and the introduction of delegated transactions aims to provide an automated and secure solution for collateral management.

## **How Delegated Transactions Work?**

1. Users can delegate specific actions related to their loans and collateral to ZeroLend through the smart contract wallet associated with their account.
2. When the collateral value approaches a critical threshold, as defined by the user, ZeroLend can autonomously execute predefined actions, such as closing the user's position to prevent liquidation.
3. Delegated transactions do not compromise the custody of user assets. ZeroLend only has permission to perform actions explicitly delegated by the user, ensuring the security of the user's holdings.

> Importantly, this delegation is secured by smart contract wallets, ensuring that ZeroLend can only execute specific delegated transactions and cannot access or misappropriate user assets.

{% hint style="info" %}
ZeroLend is set to implement this feature in 2024.&#x20;
{% endhint %}
