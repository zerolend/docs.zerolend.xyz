---
description: This section explains about the audits done for ZeroLend
cover: ../.gitbook/assets/Tokenomics GITBOOK Size.png
coverY: 0
---

# Audits

ZeroLend is a dynamic lending protocol that closely resembles Aave V3. It was developed as a fork from the original Aave protocol. As a result, ZeroLend inherits the battle-tested and audited smart contract codebase from Aave V3.

Since ZeroLend doesn't introduce any changes or modifications to the existing code, it benefits from the extensive audits conducted on Aave V3. This strong foundation ensures the security and reliability of ZeroLend's protocol, providing users with a trusted and proven lending platform without the need for additional audits.

The ZeroLend team has further taken steps to secure the protocol by conducting external audits with reputed third-party auditors [Mundus.dev](https://mundus.dev/) and [Peckshield](https://peckshield.com/).&#x20;

## External Audit by Mundus. dev

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

## External Audit by Peckshield&#x20;

Peckshield conducted an in-depth audit for ZeroLend. It analyzed coding bugs, executed semantic checks, and performed advanced DeFi scrutiny (including Oracle security, business logic, and escrow).&#x20;

In our audit, Peckshield highlighted 8 medium—to low-severity issues: medium (2), Low (5), and Informational (1).&#x20;

Peckshield concluded that ZeroLend smart contracts are well-designed and engineered, though resolving the identified issues can improve their implementation.&#x20;

Please note that those identified issues are promptly confirmed and addressed.&#x20;

Read ZeroLend's Peckshield Audit report on our GitHub page:&#x20;

{% embed url="https://github.com/zerolend/audits/tree/main/peckshield" %}

## Existing Audits from Aave

By leveraging the well-established codebase of Aave V3, ZeroLend can focus on delivering a seamless and user-friendly experience while upholding the highest standards of safety in the DeFi space.

You can find a list of audits done over here:

| Auditor Report                                                                                                     | Audit Type          | Date                    |
| ------------------------------------------------------------------------------------------------------------------ | ------------------- | ----------------------- |
| [ABDK](https://github.com/aave/aave-v3-core/blob/master/audits/27-01-2022_ABDK_AaveV3.pdf)                         | Smart Contract      | 01-27-2022              |
| [SigmaPrime](https://github.com/aave/aave-v3-core/blob/master/audits/27-01-2022_SigmaPrime_AaveV3.pdf)             | Smart Contract      | 01-27-2022              |
| [Certora](https://github.com/aave/aave-v3-core/blob/master/certora/Aave_V3_Formal_Verification_Report_Jan2022.pdf) | Formal Verification | 11-12-2021 - 01-24-2022 |
| [Peckshield](https://github.com/aave/aave-v3-core/blob/master/audits/14-01-2022_PeckShield_AaveV3.pdf)             | Smart Contract      | 01-14-2022              |
| [Trail of Bits](https://github.com/aave/aave-v3-core/blob/master/audits/07-01-2022_TrailOfBits_AaveV3.pdf)         | Smart Contract      | 01-07-2022              |
| [OpenZeppelin](https://github.com/aave/aave-v3-core/blob/master/audits/01-11-2021_OpenZeppelin_AaveV3.pdf)         | Smart Contract      | 01-11-2021              |

## External Audits from Halborn Security

ZeroLend engaged [Halborn](https://halborn.com/)—a specialized blockchain security firm—to address two primary challenges: securing our smart contracts from potential vulnerabilities and managing the complexity of a multi-chain, Layer-2 environment.

**Scope & Methodology**

* **Comprehensive Code Review**: Halborn conducted a thorough audit of ZeroLend’s smart contracts, focusing on potential attack vectors and logic flaws.
* **Layer-2 & Multi-Chain Expertise**: The engagement included specialized consulting on multi-chain integrations and L2-specific security considerations.
* **Ongoing Support**: Halborn utilized a Security-as-a-Service (SAaaS) model, providing live assistance and detailed guidance throughout the process.

**Key Findings & Outcomes**

* **Logic Flaw Prevention**: A critical flaw in ZeroLend’s staking contract was identified and rectified before any exploitation could occur.
* **Enhanced Security Awareness**: Halborn provided comprehensive security training, boosting internal best practices and cultivating a security-first culture.
* **Future-Proofing**: Their proactive approach mitigated not only current vulnerabilities but also potential future threats as ZeroLend grows.

#### Read the Case Study

{% embed url="https://www.halborn.com/case-studies/post/case-study-strengthening-zerolend-s-multi-chain-lending-platform-with-halborn" %}

## External Audits from Zokyo

ZeroLend  partnered with [Zokyo Security](https://zokyo.io/) to perform an in-depth assessment of our smart contracts. This audit further validated the robustness of our code and identified areas to strengthen.

**Scope & Highlights**

* **Comprehensive Coverage**: Zokyo achieved **100% testable code coverage**, surpassing industry standards.
* **Zero Critical or High Vulnerabilities**: The audit found no issues classified as critical or high, underscoring the platform’s reliability.
* **Actionable Recommendations**: Zokyo provided a set of recommendations to enhance ZeroLend’s security posture, all of which are being implemented.

**Key Takeaways**

* **Reinforced Code Integrity**: Passing the Zokyo audit with zero critical findings confirms ZeroLend’s core functionality is secure.
* **Continuous Improvement**: Implementation of recommended improvements ensures that our protocol evolves alongside emerging threats.
* **Public Transparency**: A summary of the audit is available for community review, reflecting our commitment to openness.

#### Read the report:

{% embed url="https://zokyo.io/reports/zerolend" %}

## Bug Bounty Contests&#x20;

ZeroLend also organized bug bounty contests in collaboration with the leading bug bounty platforms. These contests invite white-hat security analysts to dive deep into our codebase to find vulnerabilities.&#x20;

We hosted bug bounty competitions on Cantina and Immunefi with a combined reward pool of nearly $300,000.

Cantina Bug Bounty: [https://twitter.com/cantinaxyz/status/1743332737074020704](https://twitter.com/cantinaxyz/status/1743332737074020704)

Immunefi Bug Bounty: [https://twitter.com/zerolendxyz/status/1761072126776488023](https://twitter.com/zerolendxyz/status/1761072126776488023)\
