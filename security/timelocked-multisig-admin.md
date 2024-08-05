---
description: >-
  This page discusses the timelock admin contract that governs ZeroLend’s
  administrative functions.
---

# Timelocked Multisig Admin

ZeroLend uses a time lock mechanism on all administrative functions, including proxy contracts, to strengthen our protocol’s security. A multi-signature contract oversees our timelock mechanism.

A time-locked multi-sig admin will secure our protocol until we introduce decentralized governance to govern ZeroLend. Any transaction proposal requires a consensus of at least three out of five authorized parties (previously, from two out of three). The proposed transaction becomes executable only after a designated 5-day waiting period (from a 24-hour waiting period previously), which can be extended if necessary.

Here are the contract addresses for your reference:

* Timelock Contract: [0x861cC6724D0aA7Ec7a868887643e682b1c16aeeC](https://era.zksync.network/address/0x861cC6724D0aA7Ec7a868887643e682b1c16aeeC) (Old) [0x00000ab6ee5a6c1a7ac819b01190b020f7c6599d](https://lineascan.build/address/0x00000ab6ee5a6c1a7ac819b01190b020f7c6599d) (New)
* Safe Contract (Multisig): [0x1890F9204882dfa1B8f0AEaF56ae9b2ed149D18d](https://app.safe.global/transactions/history?safe=zksync:0x1890F9204882dfa1B8f0AEaF56ae9b2ed149D18d) (Old) [0x14aAD4668de2115e30A5FeeE42CFa436899CCD8A](https://safe.linea.build/settings/setup?safe=linea:0x14aAD4668de2115e30A5FeeE42CFa436899CCD8A) (New)

These wallet addresses have the authority to sign transactions within the multi-sig contract:

* ZeroLend Team #1: [0x09869dF9b616b3e60E7782f6a675d135f17051FD](https://era.zksync.network/address/0x09869df9b616b3e60e7782f6a675d135f17051fd)
* ZeroLend Team #2: [0xb76F765A785eCa438e1d95f594490088aFAF9acc](https://era.zksync.network/address/0xb76F765A785eCa438e1d95f594490088aFAF9acc)
* ZeroLend Cold Wallet: [0x6aac0942B8147BffAB73789a82EE12fDA7735BAc](https://era.zksync.network/address/0x6aac0942b8147bffab73789a82ee12fda7735bac)

The source code for the various contracts, including their deployment scripts, can be found here: [https://github.com/zerolend/governance](https://github.com/zerolend/governance)[governance](https://github.com/zerolend/governance)

{% embed url="https://github.com/zerolend/governance" %}
