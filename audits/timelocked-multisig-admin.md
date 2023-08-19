---
description: This page talks about the timelock admin contract that governs ZeroLend
---

# Timelocked Multisig Admin

To bolster our community's security measures, we've implemented a time lock mechanism on all administrative functions, including proxy contracts. This mechanism is overseen by a multi-signature contract.

A timelocked multi-sig admin is a necessary step in protecting the protocol until it gets replaced with a decentralized governance.

For any transaction proposal, a consensus of at least two out of three authorized parties is required. The proposed transaction becomes executable only after a designated 24-hour waiting period. This waiting period can be extended if deemed necessary.

Here are the contract addresses for reference:

* Timelock Contract: [0x861cC6724D0aA7Ec7a868887643e682b1c16aeeC](https://explorer.zksync.io/address/0x861cC6724D0aA7Ec7a868887643e682b1c16aeeC)
* Safe Contract (Multisig): [0x7b08d0d9D6f450243500338C39B1c9F01a30d801](https://explorer.zksync.io/address/0x7b08d0d9D6f450243500338C39B1c9F01a30d801)

The following individuals/entities have the authority to sign transactions within the multisig contract:

1. ZeroLend Team #1: [0x09869dF9b616b3e60E7782f6a675d135f17051FD](https://explorer.zksync.io/address/0x09869df9b616b3e60e7782f6a675d135f17051fd)
2. ZeroLend Team #2: [0xb76F765A785eCa438e1d95f594490088aFAF9acc](https://explorer.zksync.io/address/0xb76F765A785eCa438e1d95f594490088aFAF9acc)

These measures have been put in place to enhance the overall security and governance of our ecosystem.

The source code for the various contracts including their deployment scripts can be found here: [https://github.com/zerolend/governance](https://github.com/zerolend/governance)

{% embed url="https://github.com/zerolend/governance" %}
