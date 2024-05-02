---
description: >-
  This page will discuss Account Abstraction and how it is integrated into the
  ZeroLend protocol to enhance user experience.
---

# Account Abstraction (AA)

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

Account Abstraction (AA) is a concept that hides such complexities. In DeFi, account abstraction removes all these complexities by storing assets in smart contracts rather than externally owned accounts (EOAs). Thus, it helps developers create ‘programmable wallets.’

Technically, account abstraction enables developers to create account-abstracted wallets or smart accounts that can initiate and execute transactions on behalf of the user. For example, with smart accounts, dApps can pay gas fees on behalf of the user, saving users from the hassle of acquiring native tokens to pay gas fees.&#x20;

Unlike EOAs, which send regular transactions, smart accounts use objects called UserOperations that include metadata to describe the operation to be executed on behalf of the user. Some examples of this metadata include type of transaction, gas price, transaction signature, etc.&#x20;

Account Abstraction unlocks several use cases to improve user experience. With AA, dApps can pay gas fees on users’ behalf, users can pay gas fees in any ERC-20 token, and users can log in using social media accounts.&#x20;

## How Does ZeroLend Implement AA?

ZeroLend integrates several zkSync-native AA features in the following ways:

**Paymasters (Live on zkSync)**: Allows the protocol to subsidize or allow users to pay for transaction fees with ERC20 tokens rather than $ETH.&#x20;

**Social Logins & other authentication options** (Not Live): Allows users to have a wallet that controls their secure enclave device (Face ID, Fingerprint scanners, etc..)&#x20;

**Delegated transaction** (Not Live): Allows users to authorize ZeroLend to execute limited actions on their behalf without losing custody of their funds.

***

## Paymasters (Live)

### **What are Paymasters?**

Paymaster is a smart contract that facilitates and controls gas fee payments for transactions on behalf of wallet owners/users. With Paymasters, developers can grant users the ability to transact at zero gas fees or to use the application's native ERC-20 token for payment.

Read the [zkSync documentation](https://era.zksync.io/docs/api/python/paymaster-utils.html) for a comprehensive understanding of Paymasters and how they work.&#x20;

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

### How Does ZeroLend Use Paymasters?

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

* $HOLD (Holdstation)
* $GRAI (Gravita)
* $USDC

Secure-enclave and social logins

<figure><img src="../.gitbook/assets/ZL Doc - Verification.png" alt=""><figcaption></figcaption></figure>

## Social Logins (Not Live)

Social logins provide a user-friendly and self-custodial authentication mechanism on ZeroLend. By enabling users to link their Web2 identity with their on-chain account, we aim to lower the entry barriers for beginners. This process eliminates the need for users to interact directly with private keys, offering a seamless onboarding experience.

With social logins, end-users can effortlessly authenticate through their preferred accounts, such as email, phone number, or social media accounts. Users can easily create a smart contract wallet on ZeroLend. You no longer need to download specific wallet applications or manage seed phrases with smart contract wallets.

> We are working with Particle Network to integrate the Social Login feature into our protocol. You can read more about Authentication Infra in the [Particle Network docs](https://docs.particle.network/developers/auth-service).

## Biometrics (Not Live)

ZeroLend will support biometric authentication by incorporating fingerprint recognition and other authentication methods. Biometric authentication provides a secure and user-friendly means of verifying users' identities compared to traditional passwords and private keys. Users can easily authenticate transactions within the ZeroLend ecosystem using their biometric data.

> Anytime you need to sign a transaction, you’ll just have to enter your biometrics to complete the transaction.

{% hint style="info" %}
ZeroLend will implement a secure enclave and social logins in 2024.
{% endhint %}

***

## Delegated transaction

<figure><img src="../.gitbook/assets/ZL Doc - Delegated Transactions.png" alt=""><figcaption></figcaption></figure>

Collateral monitoring is a challenge in DeFi lending. Managing collateral and loans on platforms such as Compound requires users to continuously monitor and adjust collateral deposits to prevent losses. If the price of your deposited collateral drops below a certain threshold, it gets liquidated. This process can be demanding and stressful for users.

ZeroLend abstracts away these challenges. With Zerolend, you receive an automated and secure collateral management solution using account abstraction and delegated transactions.&#x20;

### **How Delegated Transactions Work?**

1. Users can delegate specific actions related to their loans and collateral to ZeroLend through the smart contract wallet associated with their account.
2. When the collateral value approaches a critical threshold, as defined by the user, ZeroLend will autonomously execute predefined actions. For example, you can delegate ZeroLend to close your loan position to prevent liquidation.
3. Delegated transactions do not compromise the custody of user assets. ZeroLend only has permission to perform actions explicitly delegated by the user, ensuring the security of the user's holdings.

> Smart contract wallets secure delegated transactions on our platform. ZeroLend can only execute specific delegated transactions and cannot access or misappropriate user assets.

{% hint style="info" %}
ZeroLend is set to implement this feature in 2024.&#x20;
{% endhint %}
