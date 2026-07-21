# Protocol metrics

Pulsar's dashboard should help users understand what is happening without disguising assumptions. Metrics should show their formulas, data sources, update times, and important exclusions.

## Market metrics

- **PULSAR price:** current reference price and venue.
- **Market capitalization:** price multiplied by circulating supply.
- **Fully diluted valuation:** price multiplied by the defined maximum or fully diluted supply, if applicable.
- **Liquidity and volume:** depth and activity across approved markets.

## Supply and staking metrics

- circulating, total, and maximum supply;
- amount and percentage staked;
- current epoch and next rebase time;
- reward yield per epoch;
- projected APY with explicit assumptions;
- PULSAR-to-QUASAR and wrapped-QUASAR conversion ratios;
- emission runway under stated assumptions.

## Treasury metrics

- gross, net, liquid, and risk-adjusted treasury value;
- protocol-owned liquidity by pool;
- liabilities and committed mint payouts;
- asset and strategy concentration;
- realized and unrealized performance;
- net earnings and retained earnings;
- distribution history and coverage.

## Mint metrics

- accepted asset and verified token address;
- effective mint price;
- quoted discount or premium;
- capacity, sold amount, and remaining capacity;
- payout, vesting duration, and claimable amount;
- valuation source and applied haircut.

## Reading APY correctly

APY compounds a current per-epoch rate over a hypothetical year. It assumes the rate continues and generally measures token growth, not guaranteed dollar growth. A five-digit APY can fall quickly when the policy rate changes, and more tokens do not guarantee more purchasing power.

Pulsar should never combine emissions and realized treasury earnings into one unlabeled “yield” number.

