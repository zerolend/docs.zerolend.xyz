---
description: This page discusses how delegated transactions work behind the scenes.
---

# Delegated transaction

<figure><img src="../../.gitbook/assets/ZL Doc - Delegated Transactions.png" alt=""><figcaption></figcaption></figure>

Collateral monitoring is a challenge in DeFi lending. Managing collateral and loans on platforms such as Compound requires users to continuously monitor and adjust collateral deposits to prevent losses. If the price of your deposited collateral drops below a certain threshold, it gets liquidated. This process can be demanding and stressful for users.

ZeroLend abstracts away these challenges. With Zerolend, you receive an automated and secure collateral management solution using account abstraction and delegated transactions.&#x20;

## **How Delegated Transactions Work?**

1. Users can delegate specific actions related to their loans and collateral to ZeroLend through the smart contract wallet associated with their account.
2. When the collateral value approaches a critical threshold, as defined by the user, ZeroLend will autonomously execute predefined actions. For example, you can delegate ZeroLend to close your loan position to prevent liquidation.
3. Delegated transactions do not compromise the custody of user assets. ZeroLend only has permission to perform actions explicitly delegated by the user, ensuring the security of the user's holdings.

> Smart contract wallets secure delegated transactions on our platform. ZeroLend can only execute specific delegated transactions and cannot access or misappropriate user assets.

{% hint style="info" %}
ZeroLend is set to implement this feature in 2024.&#x20;
{% endhint %}
