---
description: >-
  This page talks about how ZeroLend enables gasless transactions with the help
  of zkSync's native paymaster integration.
---

# Paymasters

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## **What are Paymasters?**

Paymasters are a useful tool for abstracting the payment of transaction fees on the Ethereum network. They allow users to pay for their transactions in a variety of ways, without having to hold Ether or sacrifice custody of their account.

A Paymaster, at its core, is a sophisticated smart contract. It serves as a payment facilitator, executing transactions on behalf of users while incorporating customizable logic to make informed decisions about transaction approval and payment. With Paymasters, developers can grant users the ability to transact at zero cost or to use the application's native ERC-20 token for payment.

For a comprehensive understanding of Paymasters and how they work, please refer to the zkSync documentation here[^1].

## How does ZeroLend Use Paymasters

ZeroLend uses Paymasters in two different ways.&#x20;

1. To subsidize transactions costs for users
2. To allow users to pay transaction fees with ERC20 tokens.



[^1]: 
