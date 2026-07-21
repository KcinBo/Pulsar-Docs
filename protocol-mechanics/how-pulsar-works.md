# How Pulsar works

Pulsar connects four economic systems: minting, the treasury, staking, and protocol policy.

## 1. Minting brings assets into the treasury

In a mint, a participant gives the protocol an approved asset or liquidity position in exchange for a quoted amount of newly issued PULSAR. The PULSAR may vest over time. A mint is attractive to the participant only when its effective terms compare favorably with buying PULSAR on the market.

Potential mint assets include pDAI, WPLS, USDC, PLSX, ETH or WETH, approved LP tokens, and other assets added under the protocol's authorization process. Listing an asset in these docs does not mean a market is live.

## 2. The treasury owns and manages those assets

Minted assets become protocol-controlled capital. The treasury may hold liquid reserves, own liquidity positions, or deploy capital through approved strategies. Each asset and strategy carries different risks, so treasury reporting should distinguish liquid reserves from volatile, illiquid, bridged, or productive positions.

## 3. Staking converts PULSAR into QUASAR

A holder deposits PULSAR into the staking contract and receives QUASAR. QUASAR represents the staked position. If the system uses rebasing accounting, a holder's QUASAR balance may increase at each epoch as authorized rewards are distributed.

A planned wrapped version may hold a stable wallet balance while its conversion value grows with the QUASAR index. The wrapper's final name and behavior will be documented only after implementation.

## 4. Policy controls the system

Protocol policy determines which mint markets can open, their capacity and pricing, authorized token emissions, treasury strategy limits, liquidity management, and whether realized earnings are retained or distributed.

These parts form a loop:

**value-accretive mints → treasury growth → productive deployment and liquidity → protocol earnings and support → stronger long-term alignment**

That loop can also reverse. Poor mint terms, weak markets, treasury losses, excessive token issuance, or failed strategies can reduce backing and confidence. Pulsar's reporting and governance must make both upside and downside visible.

