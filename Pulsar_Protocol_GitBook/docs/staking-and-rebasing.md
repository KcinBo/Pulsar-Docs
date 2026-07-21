# Staking and rebasing

Staking is the process of depositing PULSAR into the staking contract and receiving QUASAR. It is intended for participants who want continued exposure to the protocol and its authorized reward system.

## The basic flow

1. Connect a supported wallet to the official Pulsar application.
2. Confirm the PULSAR staking contract address from the official Contracts page.
3. Approve PULSAR for use by the staking contract.
4. Choose an amount and submit the stake transaction.
5. Receive QUASAR after the transaction confirms.

To exit, the holder submits QUASAR to the staking contract and receives the corresponding amount of PULSAR under the contract's current conversion rules.

> The application, contract addresses, transaction steps, and approvals described here are placeholders until deployment. Never interact with an address copied from social replies, private messages, or unofficial token lists.

## What is a rebase?

A rebase updates staker accounting at a scheduled interval called an **epoch**. In a classic rebasing design, new rewards sent to the staking system increase each holder's QUASAR balance proportionally. No manual claim is required.

If you owned 1% of all eligible QUASAR immediately before a proportional distribution, you would ordinarily receive about 1% of the QUASAR allocated for that epoch, subject to contract rules and rounding.

A rebase changes token accounting. It does not create outside revenue by itself.

## Emissions are not earnings

Pulsar will distinguish two possible reward sources:

- **Token emissions:** newly issued PULSAR distributed through the staking system. These increase token balances and total supply.
- **Treasury-funded value:** realized earnings used for a distribution, market buyback, liquidity support, or another approved mechanism.

Both may benefit participants, but they are economically different. A high token-denominated APY can coexist with a falling market value if issuance, demand, and treasury growth are out of balance.

## APY and reward yield

Reward yield is the estimated percentage increase for one epoch. APY annualizes the current rate using compounding assumptions. It is a projection, not a promised cash return, and can change whenever protocol policy changes.

Before staking, consider smart-contract risk, token-price volatility, dilution, liquidity, reward-rate changes, tax treatment, and the cost of entering or leaving the position.

