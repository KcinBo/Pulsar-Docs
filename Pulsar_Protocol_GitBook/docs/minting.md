# Minting PULSAR

Minting is how Pulsar may acquire assets directly from participants. In exchange for an approved asset or liquidity position, the protocol quotes a PULSAR payout that may vest over a defined period.

Economically, this resembles the bonding mechanism used by early Olympus-style protocols. The participant is selling assets to the treasury and receiving newly issued PULSAR under the market's published terms.

## Reserve mints

A reserve mint accepts a single approved asset. Potential markets may include:

- pDAI, commonly called Pulse DAI;
- WPLS;
- USDC, with the exact chain and token representation disclosed;
- PLSX;
- ETH or WETH, as required by implementation;
- other assets authorized later.

Each market should disclose the accepted token contract, oracle and valuation method, capacity, maximum payout, vesting duration, pricing method, and major asset-specific risks.

## Liquidity mints

A liquidity mint accepts an approved LP token or other liquidity position. This can help the treasury build protocol-owned liquidity and earn trading fees. LP valuation is more complicated because it includes price exposure, impermanent loss, smart-contract risk, and—in a PULSAR pair—circular exposure to the protocol token itself.

## How to evaluate a mint

Do not look only at a displayed discount. Consider:

- the effective PULSAR price implied by the mint;
- how long the payout vests;
- price risk during vesting;
- whether rewards can be staked while vesting;
- transaction and liquidity costs;
- the reliability of the pricing oracle;
- whether a spot purchase would be simpler or cheaper.

A positive discount at entry does not guarantee profit. PULSAR's market price may fall below the effective mint price before the payout becomes available.

## Why the protocol mints

A mint is valuable to Pulsar only when the risk-adjusted value received by the treasury justifies the new PULSAR issued. Weak pricing or excessive capacity can dilute holders faster than the treasury grows. Markets should therefore have asset-specific limits and transparent accounting.

> No mint market is live unless it appears in the official application and its contract is verified on the Contracts page.

