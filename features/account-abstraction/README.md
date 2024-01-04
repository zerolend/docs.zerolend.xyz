---
description: This page talks about integrating Account Abstraction into our codebase.
---

# Account Abstraction

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Account abstraction is a blockchain technology that allows users to use smart contracts as their accounts. ZeroLend's integration of Account Abstraction technology is all set to eliminate gas fees and further integrate this technology with the rest of it's products.&#x20;

To facilitate a frictionless transition into the gas-free era, ZeroLend is diligently integrating Account Abstraction technology into its various frontends. This integration does not modify any of the smart-contract logic of the protocol but instead allows the frontend to interact with the protocol in more user-friendly ways.

## How Does ZeroLend Implement AA?

ZeroLend integates various zkSync-native AA features in the following ways:

* [Paymasters](../gasless-transactions.md): Allows the protocol to either subsidize or allow users to pay for transaction fees with ERC20 tokens without having any ETH in their wallets.
* [Social Logins / Secure-Enclave wallets](login-with-face-id-socials.md): Allows users to have a wallet that is in control with their secure enclave device (Face ID, Fingerprint scanners etc..)
