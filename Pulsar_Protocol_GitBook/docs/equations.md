# Equations and methodology

These formulas explain the intended concepts. They are not final contract specifications. The production documentation must be updated to match audited code, precision rules, oracle behavior, and front-end calculations.

## Staking rewards

`reward yield per epoch = PULSAR distributed to eligible stakers / eligible staked PULSAR`

If an epoch reward yield is `r` and there are `n` epochs per year:

`projected APY = (1 + r)^n - 1`

For three epochs per day, `n = 1,095`. The final Pulsar epoch schedule has not been set in these docs.

## Index and wrapper

The index represents how a staked unit at the starting index would have grown through rebases.

Conceptually:

`QUASAR represented by wrapped QUASAR = wrapped balance × current index conversion factor`

Exact wrapping and unwrapping formulas remain pending.

## Mint payout

`mint payout = risk-adjusted value of asset supplied / effective mint price`

A policy curve may use debt, capacity, time, or demand to change the price. Do not assume the historical Olympus bond-control formula will be used unless the deployed contracts implement it.

## Treasury backing

`gross backing per circulating PULSAR = gross treasury value / circulating PULSAR`

`net backing per circulating PULSAR = (counted treasury assets - liabilities) / circulating PULSAR`

`risk-adjusted backing = [sum(asset market value × approved haircut) - liabilities] / circulating PULSAR`

These are accounting metrics. They do not create a redemption right or guaranteed price floor.

## Treasury earnings

`net treasury earnings = realized income + realized gains - realized losses - operating expenses - risk provisions`

`distributable earnings = max(0, net treasury earnings - retained earnings requirement - reserve replenishment)`

`approved distribution = distributable earnings × authorized distribution percentage`

The actual framework may include high-water marks, period-specific losses, taxes, performance fees, or other adjustments after legal, accounting, and governance review.

## Emission runway

Runway estimates how long a reward policy could continue under stated assumptions. It is highly sensitive to treasury valuation, supply growth, staking percentage, reward rate, and asset prices. It should be treated as a scenario estimate, not a countdown guarantee.

