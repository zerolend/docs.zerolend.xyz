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

# Redstone

## Using Redstone Oracles

RedStone is a multi-chain Oracle service that provides frequently updated, reliable, and diverse data feeds. ZeroLend utilizes price feeds from Redstone Oracles to calculate collateral value and liquidations.

RedStone protects all ZeroLend's markets on Zircuit, Manta, and Blast and also provides LRT feeds on ETH mainnet and Linea. ZeroLend also uses LBTC / BTC feed from RedStone on Base. You can find the exact contract addresses in RedStone Docs:

{% embed url="https://docs.redstone.finance/docs/smart-contract-devs/price-feeds" %}

### Asset-Specific Oracle Information

#### **$STONE**&#x20;

For $STONE on ZeroLend, RedStone provides oracle price feeds essential for market operations.

* Overview:[ $STONE on ZeroLend](https://app.zerolend.xyz/reserve-overview/?underlyingAsset=0xec901da9c68e90798bbbb74c11406a32a70652c3\&marketName=proto_manta_v3)
* Oracle Address:[ RedStone Oracle for $STONE](https://pacific-explorer.manta.network/address/0x36c44B353a340fbC5c7a6A0b8C56269CAC6967A3)

**$wUSDM**&#x20;

RedStone provides $wUSDM price feed for [ZeroLend's Manta Market](https://app.zerolend.xyz/?marketName=proto_manta_v3), ensuring reliable and up-to-date pricing information.

* Overview:[ $wUSDM on ZeroLend](https://app.zerolend.xyz/reserve-overview/?underlyingAsset=0xbdad407f77f44f7da6684b416b1951eca461fb07\&marketName=proto_manta_v3)
* Oracle address:[ RedStone Oracle for $wUSDM](https://pacific-explorer.manta.network/address/0x06D3ddB240A0848FF6d6952742fe814306F86356)
