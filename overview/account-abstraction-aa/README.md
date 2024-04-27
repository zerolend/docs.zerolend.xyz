---
description: >-
  This page will discuss Account Abstraction and how it is integrated into the
  ZeroLend protocol to enhance user experience.
---

# Account Abstraction (AA)

<figure><img src="../../.gitbook/assets/ZL Doc - Account Abstraction.png" alt=""><figcaption></figcaption></figure>

The DeFi ecosystem can be complex for beginners because it involves storing seed phrases, bridging crypto to different chains, paying gas fees in native tokens, etc. Therefore, enhancing the user experience of DeFi applications and making them as intuitive as TradFi applications is crucial to increasing user adoption.

There are two types of accounts in Ethereum:

1. Smart contract accounts where developers store their code (smart contracts).
2. Externally owned accounts (EOAs) where users store their tokens (wallets like Metamask).

Users interact with DApps using EOA wallets, the only way to start a transaction or execute a smart contract code. However, using this approach has many downsides:&#x20;

* The wallets are tightly coupled with a single key.
* Wallets are hard to secure as private keys might get compromised.
* Wallet keys cannot be recovered if lost. &#x20;
* Wallets don't support multi-sig.
* Users cannot use social logins.&#x20;
* Users must pay gas fees.&#x20;
* Users must have $ETH or other native chain tokens to pay gas fees.&#x20;

Account Abstraction (AA) is a computer science concept that hides such complexities. In DeFi, account abstraction removes all these complexities by storing assets in smart contracts rather than externally owned accounts (EOAs). Thus, it helps developers create ‘programmable wallets.’

Technically, account abstraction enables developers to create account-abstracted wallets or smart accounts that can initiate and execute transactions on behalf of the user. For example, with smart accounts, dApps can pay gas fees on behalf of the user, saving users from the hassle of acquiring native tokens to pay gas fees.&#x20;

Unlike EOAs, which send regular transactions, smart accounts use objects called UserOperations that include metadata to describe the operation to be executed on behalf of the user. Some examples of this metadata include type of transaction, gas price, transaction signature, etc.&#x20;

Account Abstraction unlocks several use cases to improve user experience. For example, with AA, DApps can pay gas fees on users’ behalf, users can pay gas fees in any ERC-20 token, users can login using social media accounts, etc.&#x20;

## Does zkSync support Account Abstraction?

zkSync supports native Account Abstraction. Native Account Abstraction on zkSync fundamentally changes how accounts operate by introducing the concept of Smart Accounts and Paymasters.

The differences between Native Account Abstraction and EIP 4337:

| Aspect                 | zkSync Native AA                                                                                           | Ethereum EIP 4337                                                                                                          |
| ---------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Implementation         | Integrated at protocol level                                                                               | Avoids protocol-level implementation                                                                                       |
| Account Types          | All accounts, including EOAs, behave like smart contract accounts; support paymasters                      | Separate transaction flow for smart contract accounts; EOAs lack paymaster support                                         |
| Transaction Processing | Unified mempool, Operator bundles transactions for both EOAs and smart contracts, leading to a single flow | Separate mempool for smart contract accounts, Bundlers send user operations to EntryPoint contract, resulting in two flows |
| Paymasters Support     | Supports paymasters for both EOAs and smart contract accounts                                              | No paymaster support for EOAs; implemented only for smart contract accounts in a new transaction flow                      |

## How Does ZeroLend Implement AA?

ZeroLend integrates several zkSync-native AA features in the following ways:

[Paymasters](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/account-abstraction-aa/paymasters): Allows the protocol to subsidize or allow users to pay for transaction fees with ERC20 tokens rather than $ETH.&#x20;

[Social Logins & other authentication options](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/account-abstraction-aa/login-with-face-id-socials): Allows users to have a wallet that controls their secure enclave device (Face ID, Fingerprint scanners, etc..)

[Delegated transaction](https://app.gitbook.com/o/Akzp3BDVzd6MoCyLbMoK/s/i9DDwWcSwiiTEJZZlm8R/\~/changes/126/features/account-abstraction-aa/delegated-transaction): Allows users to authorize ZeroLend to execute limited actions on their behalf without losing custody of their funds.
