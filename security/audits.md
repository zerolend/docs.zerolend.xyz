---
description: This section explains about the audits done for ZeroLend
---

# Audits

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p><a href="https://mundus.dev/">https://mundus.dev/</a></p></figcaption></figure>

ZeroLend is a dynamic lending protocol that closely resembles Aave V3, developed as a fork from the original Aave protocol. As a result, ZeroLend inherits the battle-tested and audited smart contract codebase from Aave V3.&#x20;

Since ZeroLend doesn't introduce any changes or modifications to the existing code, it benefits from the extensive audits conducted on Aave V3. This strong foundation ensures the security and reliability of ZeroLend's protocol, providing users with a trusted and proven lending platform without the need for additional audits.&#x20;

The ZeroLend team has further taken a step to secure the protocol by conducting an extra external audit with [Mundus.dev](https://mundus.dev/), a well-known 3rd party auditor for auditing lending protocol and Aave forks.

## External Audit by Mundus.dev

The scope of the audit by [Mundus](https://mundus.dev/) was to ensure that the protocol that was deployed on the zkSync mainnet and the original codebase from Aave are the same and that there are:

* No code changes were made from what was deployed and the original Aave source code.
* No backdoors that have been created by the team
* No EOA (Externally owned Account) ownership on any of the smart-contracts

The following scope resulted in the report below:

{% embed url="https://github.com/zerolend/audits/blob/main/mundus/zerolend_report_depcheck_final.pdf" %}

Following the report, all ownership of the protocol have been moved into a [Timelock contract and Multisig wallet](timelocked-multisig-admin.md).

{% embed url="https://twitter.com/zerolendxyz/status/1699619482447290547" %}

## Existing Audits from Aave

By leveraging the well-established codebase of Aave V3, ZeroLend can focus on delivering a seamless and user-friendly experience while upholding the highest standards of safety in the DeFi space.

You can find a list of audits done over here:

| Auditor Report                                                                                                          | Audit Type          | Date                    |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------- | ----------------------- |
| [ABDK](https://github.com/aave/aave-v3-core/blob/master/audits/27-01-2022\_ABDK\_AaveV3.pdf)                            | Smart Contract      | 01-27-2022              |
| [SigmaPrime](https://github.com/aave/aave-v3-core/blob/master/audits/27-01-2022\_SigmaPrime\_AaveV3.pdf)                | Smart Contract      | 01-27-2022              |
| [Certora](https://github.com/aave/aave-v3-core/blob/master/certora/Aave\_V3\_Formal\_Verification\_Report\_Jan2022.pdf) | Formal Verification | 11-12-2021 - 01-24-2022 |
| [Peckshield](https://github.com/aave/aave-v3-core/blob/master/audits/14-01-2022\_PeckShield\_AaveV3.pdf)                | Smart Contract      | 01-14-2022              |
| [Trail of Bits](https://github.com/aave/aave-v3-core/blob/master/audits/07-01-2022\_TrailOfBits\_AaveV3.pdf)            | Smart Contract      | 01-07-2022              |
| [OpenZeppelin](https://github.com/aave/aave-v3-core/blob/master/audits/01-11-2021\_OpenZeppelin\_AaveV3.pdf)            | Smart Contract      | 01-11-2021              |
