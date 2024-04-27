---
description: >-
  This page discusses how ZeroLend enables gasless transactions using zkSync's
  native paymaster integration.
---

# Paymasters

## **What are Paymasters?**

Paymaster is a smart contract that facilitates and controls gas fee payments for transactions on behalf of wallet owners/users. With Paymasters, developers can grant users the ability to transact at zero gas fees or to use the application's native ERC-20 token for payment.

Read the [zkSync documentation](https://era.zksync.io/docs/api/python/paymaster-utils.html) for a comprehensive understanding of Paymasters and how they work.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## How Does ZeroLend Use Paymasters?

ZeroLend harnesses the power of zkSync Paymasters in two key ways:

1. #### **Sponsoring Gas Fees:**&#x20;

ZeroLend utilizes the**`validatePaymasterOp(UserOperation op)`**method of the zkSync Paymaster contract to examine a user's operation. It helps us determine whether the user's transaction is valid so we can cover the associated gas fees.

{% hint style="info" %}
&#x20;ZeroLend sponsors the gas fees for users with transactions above $5000.
{% endhint %}

2. **Pay gas fees using ERC-20 tokens:**&#x20;

ZeroLend enables users to pay gas fees in $ETH and other supported tokens by integrating[ Zyfi's paymaster API](https://zyfi.org/). After the user signs the transaction and selects an ERC-20 token to pay the gas fee, ZeroLend communicates with Zyfi's Paymaster API and executes transactions, covering $ETH gas fees while utilizing ERC-20 tokens for the associated fees.&#x20;

For example, if a user wants to lend $DAI but does not have $ETH for gas fees, they use $DAI to pay gas fees on ZeroLend.&#x20;

Currently, we support the following ERC-20 tokens that can be used as gas tokens:

* $HOLD
* $DAI
* $USDC
* $ONEZ

