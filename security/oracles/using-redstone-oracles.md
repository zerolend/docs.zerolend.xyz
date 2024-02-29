---
description: >-
  This page talks about how ZeroLend uses RedStone as one it's oracle price
  feeds provider.
---

# Using Redstone Oracles

<figure><img src="../../.gitbook/assets/RedStone_main logo.svg" alt=""><figcaption></figcaption></figure>

ZeroLend utilizes price feeds from Redstone Oracles to calculate the collateral value and liquidations.

All ZeroLend's markets on Manta L2 are protected by RedStone. You can find the exact contract addresses in RedStone Docs:

{% embed url="https://docs.redstone.finance/docs/smart-contract-devs/price-feeds" %}

### Market-Specific Oracle Information

**STONE Market**

For the STONE market on ZeroLend, RedStone provides the oracle price feeds essential for market operations.

* Market Overview: [STONE Market on ZeroLend](https://app.zerolend.xyz/reserve-overview/?underlyingAsset=0xec901da9c68e90798bbbb74c11406a32a70652c3\&marketName=proto\_manta\_v3)
* Oracle Address: [RedStone Oracle for STONE](https://pacific-explorer.manta.network/address/0x36c44B353a340fbC5c7a6A0b8C56269CAC6967A3)

**wUSDM Market**

The wUSDM market utilizes RedStone for its oracle price feeds, ensuring reliable and up-to-date pricing information.

* Market Overview: [wUSDM Market on ZeroLend](https://app.zerolend.xyz/reserve-overview/?underlyingAsset=0xbdad407f77f44f7da6684b416b1951eca461fb07\&marketName=proto\_manta\_v3)
* Oracle Address: [RedStone Oracle for wUSDM](https://pacific-explorer.manta.network/address/0x06D3ddB240A0848FF6d6952742fe814306F86356)
