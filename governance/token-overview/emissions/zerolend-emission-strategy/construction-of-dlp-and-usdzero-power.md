---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Construction of dLP & $ZERO Power

ZeroLend's dLP power, closely mirroring Radiant Capital's model, is a pivotal metric in determining a user's influence within the protocol and their corresponding emissions rewards. Here's a streamlined explanation of how it works:

**dLP Power Calculation (P\_dLP)**

* **dLP Power (P\_dLP)**: This metric reflects a user's share of the total dLP pool, adjusted by a locking multiplier to reward longer commitments.

&#x20;$$P_{dLP} = dLP_{tp} \times L_{dLP} = \frac{dLP}{\textrm{Total dLP}} \times L_{dLP}$$

* $$P_{dLP}$$ is the user's total percentage of dLP relative to the entire pool.
* $$L_{dLP}$$ is the locking multiplier, enhancing power with longer lock periods.

{% hint style="info" %}
The longer the user locks dLP, the greater the power they have and ultimately the greater the emissions the user receives.
{% endhint %}

**Single-Staked $ZERO Power (P\_Z)**

* **$ZERO Power (P\_Z)**: Similar to dLP power, this calculates a user's stake in the total $ZERO pool, also influenced by the duration of the stake.&#x20;

$$
P_{Z} = \$\textrm{ZERO}_{tp} \times L_{Z} = \frac{\$\textrm{ZERO}}{\textrm{Total ZERO}} \times L_{Z}
$$

The following are the weighting coefficients:

| Time Lock | L\_d-Value | L\_z - Value |
| --------- | ---------- | ------------ |
| 1-Months  | 2          | 0.5          |
| 3-Months  | 6          | 1.5          |
| 6-Months  | 12         | 3            |
| 12-Months | 24         | 6            |
| 24-months | n/a        | 12           |
| 48-months | n/a        | 24           |

### **Combining Powers for Total Protocol Power**

By integrating both dLP and $ZERO powers, the total Protocol Power is derived, factoring in both contributions and their respective locking multipliers.

$$
P = P_{dLP} + P_{Z} = dLP_{tp} \times L_{dLP} + \$\textrm{ZERO}_{tp} \times L_{Z} \\  \hspace{2em}\\= \frac{dLP}{\textrm{Total dLP}} \times L_{dLP} + \frac{\$\textrm{ZERO}}{\textrm{Total ZERO}} \times L_{Z}\hspace{0.8em}
$$

### Final Equation for Protocol Power

$$
\textrm{Protocol Power} = (P)  \times f(T_p) \\ = (\frac{dLP}{\textrm{Total dLP}} \times L_{dLP} + \frac{\$\textrm{ZERO}}{\textrm{Total ZERO}} \times L_{Z}) \times f(4 \times \frac{\$\textrm{ZERO}_2 \times 2}{Deposits} + 1 \times \frac{\$\textrm{ZERO}_1}{Deposits})
$$

This formula underscores the significance of both liquidity provision and single asset staking in enhancing a user's impact on the protocol's governance and reward distribution, thereby incentivizing long-term participation and investment.

{% hint style="warning" %}
This functionality is scheduled to go live shortly.&#x20;
{% endhint %}
