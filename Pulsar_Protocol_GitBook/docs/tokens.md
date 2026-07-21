# PULSAR, QUASAR, and wrapped QUASAR

## PULSAR

PULSAR is the liquid protocol token. It can be held, transferred, traded, used in approved liquidity pools, deposited into the staking contract, or used in future integrations.

PULSAR's market price is set by buyers and sellers. Treasury backing, expected growth, emissions, liquidity, utility, governance, and market sentiment may all influence that price. None of them guarantees a minimum market value.

## QUASAR

QUASAR is the staked representation of PULSAR.

Under the planned model:

- stake PULSAR to receive QUASAR;
- hold QUASAR to participate in authorized staking distributions;
- unstake QUASAR to receive the corresponding PULSAR;
- use the protocol index or conversion ratio to understand how the position has changed.

The final exchange mechanics, rebase schedule, reward source, and rounding rules must match the deployed contracts.

## Future wrapped QUASAR

A wrapped version of QUASAR may be introduced for applications that work better with a non-rebasing balance. Instead of increasing the number of tokens in the wallet, the wrapped token would generally represent an increasing amount of QUASAR as the index changes.

Conceptually:

`wrapped QUASAR value = wrapped token balance × current QUASAR conversion ratio`

The wrapper name, ticker, contract, conversion formula, supported networks, and integration risks are not final. Until an official deployment is announced, any token claiming to be wrapped QUASAR should be treated as unaffiliated and potentially malicious.

## Token status

| Token | Role | Status |
|---|---|---|
| PULSAR | Liquid protocol token | Contract pending |
| QUASAR | Staked PULSAR representation | Contract pending |
| Wrapped QUASAR | Planned non-rebasing wrapper | Name and contract pending |

