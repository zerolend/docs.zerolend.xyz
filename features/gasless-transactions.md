---
description: >-
  This page talks about how ZeroLend enables gasless transactions with the help
  of zkSync's native paymaster integration.
---

# Gasless Transactions

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

### **What is a Paymaster?**

A Paymaster, at its core, is a sophisticated smart contract. It serves as a payment facilitator, executing transactions on behalf of users while incorporating customizable logic to make informed decisions about transaction approval and payment. With Paymasters, developers can grant users the ability to transact at zero cost or to use the application's native ERC-20 token for payment.

### **Evolution of Paymaster: From Account Abstraction to zkSync**

Originally conceptualized as an extension of the Account Abstraction EIP (EIP-4337), the Paymaster feature has been seamlessly integrated into zkSync. While Paymasters were initially conceived as part of the Account Abstraction proposal, our implementation introduces core differences that set it apart. To gain a deeper understanding of these distinctions, we encourage you to explore our detailed document here[^1].

### **Customized Approach: Key Objectives**

Our Paymaster system follows a customized approach that emphasizes several crucial objectives:

1. **Security and User Experience:** Above all, our primary concern is to ensure the security of user transactions. Simultaneously, we are dedicated to providing a user-friendly interface that simplifies the transaction process.
2. **Flexibility for Paymasters and Developers:** ZeroLend's Paymaster system offers an exceptional degree of flexibility. This empowers Paymasters and developers to tailor transaction payment logic to their precise needs, fostering innovation within our ecosystem.
3. **DoS (Denial of Service) Safety:** Protecting against potential DoS attacks is paramount. Our Paymaster system is fortified to effectively mitigate these threats, ensuring the uninterrupted functionality of our protocol.

### **Implementing Paymasters: The IPaymaster Interface**

To harness the capabilities of Paymasters, developers can implement the IPaymaster interface, which encompasses the following crucial methods:

* **validateAndPayForPaymasterTransaction:** This pivotal method acts as the gatekeeper, determining whether the Paymaster approves the payment for a given transaction. It plays a crucial role in maintaining security and control over transaction execution.
* **postOp:** After a transaction has been successfully executed, developers can employ the postOp method to carry out additional actions. These actions may include refunding the sender for unused resources or executing specific post-transaction operations as required.

### **In Summary**

Paymasters are a pivotal component of our ecosystem, enhancing the user experience by providing transaction payment flexibility. Simultaneously, they uphold robust security measures to safeguard against potential threats. Developers are encouraged to explore and implement the IPaymaster interface, enabling them to customize transaction payment logic and actively contribute to the growth of our decentralized lending protocol.

For a comprehensive understanding of Paymasters and their integration into our platform, please refer to our detailed documentation here[^2].

### **Additional Resources**

* **Paymaster Best Practices**: A guide to implementing Paymasters effectively for optimal user experience.
* **Paymaster Use Cases**: Real-world scenarios showcasing the versatility and advantages of Paymasters within our ecosystem.
* **Paymaster FAQs**: Answers to commonly asked questions about Paymasters and their role within ZeroLend.

[^1]: thelinkgoeshere

[^2]: Thelinkgoeshere

    &#x20;&#x20;
