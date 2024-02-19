---
description: >-
  In this portion of the document, we will define the calculation for protocol
  weight with respect to emissions.
---

# Protocol Power/Weight

Protocol Power specifically refers to the influence users have over ZeroLend's governance and operational decisions. The calculation of total protocol power is as follows:

$$
\textrm{Protocol Power} = (\textrm{dLP Power} +\$\textrm{ZERO Power}) \times f(T_p)
$$

where,&#x20;

$$
f(T_p) = f(4 \times dLP_p+1\times Z_p) = \begin{cases} 
0 & \text{if } 0.00 \leq T_p< 0.10 \\ 0.5 & \text{if } 0.10 \leq T_p <0.15\\ 0.75 & \text{if } 0.15 \leq T_p < 0.20 \\ 1.0 & \text{if } 0.20 \leq T_p <0.25\\ 1.1 & \text{if } 0.25 \leq T_p < 0.30 \\ 1.25 & \text{if } 0.30 \leq T_p <0.40\\ 1.5 & \text{if } 0.40 \leq T_p < 0.50 \\ 2.0 & \text{if } 0.50 \leq T_p \\

\end{cases}
$$

We prioritize liquidity provision by offering enhanced incentives for dLP locking over single asset staking. The formula assesses dLP and $ZERO percentages (dLP\_p and Z\_p) locked against the USD value of users' lending deposits, favoring dLP locking fourfold for two key reasons:

1. LP tokens contribute more significantly to ZeroLend's liquidity and overall ecosystem health.
2. LP tokens carry more risk due to impermanent loss

Traditionally, a maximum APR for dLP at 5% of deposited assets is now extendable up to 12.5%, with the option to boost this further by locking $ZERO tokens, whose USD value is considered four times for this purpose, enhancing rewards for users taking on the additional risk of LP staking
