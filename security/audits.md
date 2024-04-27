---
description: This section discusses ZeroLend’s security audits in detail.
cover: ../.gitbook/assets/Tokenomics GITBOOK Size.png
coverY: 0
---

# Audits

ZeroLend is a dynamic lending protocol that closely resembles Aave V3. It was developed as a fork from the original Aave protocol. As a result, ZeroLend inherits the battle-tested and audited smart contract codebase from Aave V3.

Since ZeroLend doesn't introduce any changes or modifications to the existing code, it benefits from the extensive audits conducted on Aave V3. This strong foundation ensures the security and reliability of ZeroLend's protocol, providing users with a trusted and proven lending platform without the need for additional audits.

The ZeroLend team has further taken steps to secure the protocol by conducting external audits with reputed third-party auditors [Mundus.dev](https://mundus.dev/) and [Peckshield](https://peckshield.com/).&#x20;

### External Audit by Mundus. dev

Mundus conducted a comprehensive audit for ZeroLend, which included analyzing deployed smart contracts, Git repos, and contract storage.&#x20;

Here's a summary of findings in the Mundus audit:&#x20;

* There are no issues concerning the consistency among the codebase of verified contracts on ZeroLend.
* The forked repositories do not contain any changes to the Aave codebase that would compromise the protocol's security.
* The contents of the contracts in SoW, which are unverified by the zkSync Era explorer, have been identified and are safe to use.&#x20;
* All verified contracts have a consistent codebase.
* All verified contracts use consistent versions of respective dependencies.&#x20;
* The ZeroLend codebase contains no changes that undermine the security of logic provided by Aave.&#x20;

Visit our GitHub page to read the Mundus audit report in detail:&#x20;

{% embed url="https://github.com/zerolend/audits/blob/main/mundus/zerolend_report_depcheck_final.pdf" %}

Following the report, all ownership of the protocol has been moved into a [Timelock contract and Multisig wallet](timelocked-multisig-admin.md).

{% embed url="https://twitter.com/zerolendxyz/status/1699619482447290547" %}

### External Audit by Peckshield&#x20;

Peckshield conducted an in-depth audit for ZeroLend. It analyzed coding bugs, executed semantic checks, and performed advanced DeFi scrutiny (including Oracle security, business logic, and escrow).&#x20;

In our audit, Peckshield highlighted a total of 8 medium to low-severity issues: Medium (2), Low (5), and Informational (1).&#x20;

Peckshield concluded that ZeroLend smart contracts are well-designed and engineered, though resolving the identified issues can improve their implementation.&#x20;

Please note that those identified issues are promptly confirmed and addressed.&#x20;

Read ZeroLend's Peckshield Audit report on our GitHub page:&#x20;

{% embed url="https://github.com/zerolend/audits/tree/main/peckshield" %}

### Existing Audits from Aave

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

### Bug Bounty Contests&#x20;

ZeroLend also organized bug bounty contests in collaboration with the leading bug bounty platforms. These contests invite white-hat security analysts to dive deep into our codebase to find vulnerabilities.&#x20;

We hosted bug bounty competitions on Cantina and Immunefi with a combined reward pool of nearly $200,000.

Cantina Bug Bounty: [https://twitter.com/cantinaxyz/status/1743332737074020704](https://twitter.com/cantinaxyz/status/1743332737074020704)

Immunefi Bug Bounty: [https://twitter.com/zerolendxyz/status/1761072126776488023](https://twitter.com/zerolendxyz/status/1761072126776488023)\
