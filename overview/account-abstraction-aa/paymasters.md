---
description: >-
  How ZeroLend enables gasless transactions with the help of zkSync's native
  paymaster integration?
---

# Paymasters

## **What are Paymasters?**

The Paymaster is a smart contract designed to facilitate and control the payment of gas fees for transactions on behalf of wallet owners/users. With Paymasters, developers can grant users the ability to transact at zero cost or to use the application's native ERC-20 token for payment.

For a comprehensive understanding of Paymasters and how they work, please refer to the zkSync documentation [here](https://era.zksync.io/docs/api/python/paymaster-utils.html).

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

##

## How Does ZeroLend Use Paymasters?

ZeroLend harnesses the power of zkSync Paymasters in two key ways within its protocol:

1. #### **Sponsoring Gas Fees:**&#x20;

The zkSync Paymaster contract includes a method called **`validatePaymasterOp(UserOperation op)`**, which ZeroLend utilizes to examine a user operation and determine whether the user's transaction is valid for us to cover the associated gas fees.&#x20;

{% hint style="info" %}
&#x20;ZeroLend sponsors the gas fees for users with transactions above $5000.
{% endhint %}

2. **Pay gas fees using ERC-20 tokens:**&#x20;

ZeroLend enables users to pay gas fees in ETH and other supported tokens through the integration of [**Zyfi's paymaster API**](https://zyfi.org/). After the user signs the transaction and selects an ERC-20 token to pay the gas fee, ZeroLend communicates with Zyfi's Paymaster API and executes transactions, covering ETH gas fees while utilizing ERC-20 tokens for the associated fees. \
\
In a practical example, if a user aims to lend $DAI but lacks ETH for gas fees, they can opt to cover fees using $DAI within the ZeroLend platform.

Currently, we support the following ERC-20 tokens that can be used as gas tokens:

* $HOLD
* $DAI
* $USDC
* $ONEZ

