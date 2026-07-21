# Equations and methodology

GitBook renders the formulas on this page with KaTeX. These equations explain the intended economic concepts; they are not final contract specifications. Production documentation must match audited code, fixed-point precision, oracle behavior, and front-end calculations.

## Staking reward yield

Let $R_e$ be the PULSAR distributed during epoch $e$, and let $S_e$ be the eligible staked PULSAR for that epoch. The reward yield is:

$$r_e = \frac{R_e}{S_e}$$

If every eligible staker receives the same proportional rate, a position with an opening balance $Q_e$ would have a theoretical post-rebase balance of:

$$Q_{e+1} = Q_e\left(1+r_e\right)$$

Actual results may differ because of contract precision, eligibility timing, exclusions, and rounding.

## Projected APY

If the current per-epoch reward yield $r$ remained unchanged for $N$ epochs, the projected annual percentage yield would be:

$$\operatorname{APY}_{\mathrm{projected}} = \left(1+r\right)^N - 1$$

If the protocol used three epochs per day for 365 days, the annualized number of epochs would be:

$$N = 3 \times 365 = 1{,}095$$

This is a mathematical projection, not a promised return. It assumes a constant rate and measures token-denominated balance growth rather than purchasing-power growth.

## QUASAR index

Let $I_0$ be the starting index and $r_i$ the reward yield for epoch $i$. After $t$ epochs, the theoretical index is:

$$I_t = I_0\prod_{i=1}^{t}\left(1+r_i\right)$$

The index provides a compact record of cumulative rebasing. The production formula must use the exact scaling and precision of the staking contract.

## Wrapped QUASAR conversion

Let $W$ be a wrapped QUASAR balance and $C_t$ be the QUASAR represented by one wrapped token at time $t$:

$$Q_t = W \times C_t$$

If the wrapper uses index-based accounting, its conversion ratio may be expressed conceptually as:

$$C_t = C_0\frac{I_t}{I_0}$$

The wrapper's final name, initial conversion ratio, and implemented formula remain pending.

## Risk-adjusted mint value

For each supplied asset component $j$, let $p_j$ be its oracle price, $q_j$ its quantity, and $h_j$ its approved valuation multiplier after any haircut, where $0 \leq h_j \leq 1$:

$$V_{\mathrm{adjusted}} = \sum_{j=1}^{m} p_j q_j h_j$$

If $P_{\mathrm{mint}}$ is the effective price per PULSAR offered by the mint, the theoretical token payout is:

$$M_{\mathrm{payout}} = \frac{V_{\mathrm{adjusted}}}{P_{\mathrm{mint}}}$$

The deployed mint may also apply capacity, maximum-payout, minimum-output, debt, vesting, fee, or rounding constraints.

## Treasury backing

Let $V_{\mathrm{gross}}$ be gross counted treasury assets, $L$ counted liabilities, and $S_{\mathrm{circ}}$ circulating PULSAR supply.

Gross backing per circulating PULSAR is:

$$B_{\mathrm{gross}} = \frac{V_{\mathrm{gross}}}{S_{\mathrm{circ}}}$$

Net backing per circulating PULSAR is:

$$B_{\mathrm{net}} = \frac{V_{\mathrm{gross}}-L}{S_{\mathrm{circ}}}$$

For risk-adjusted reporting, let $V_i$ be the market value of treasury asset $i$ and $h_i$ its approved valuation multiplier:

$$B_{\mathrm{risk}} = \frac{\displaystyle\sum_{i=1}^{k} V_i h_i-L}{S_{\mathrm{circ}}}$$

These are accounting metrics. They do not create a redemption right or guaranteed market-price floor. Protocol-owned liquidity containing PULSAR requires special treatment to avoid circular valuation.

## Net treasury earnings

Let:

- $I_{\mathrm{real}}$ be realized income;
- $G_{\mathrm{real}}$ be realized gains;
- $L_{\mathrm{real}}$ be realized losses;
- $O$ be operating expenses;
- $R_{\mathrm{provision}}$ be approved risk provisions.

Then:

$$E_{\mathrm{net}} = I_{\mathrm{real}} + G_{\mathrm{real}} - L_{\mathrm{real}} - O - R_{\mathrm{provision}}$$

If $E_{\mathrm{retain}}$ is the retained-earnings requirement and $E_{\mathrm{reserve}}$ is required reserve replenishment:

$$E_{\mathrm{distributable}} = \max\!\left(0, E_{\mathrm{net}}-E_{\mathrm{retain}}-E_{\mathrm{reserve}}\right)$$

For an authorized distribution fraction $\delta$, where $0 \leq \delta \leq 1$:

$$D_{\mathrm{approved}} = \delta E_{\mathrm{distributable}}$$

The final framework may include high-water marks, previous-period losses, taxes, fees, and other legally or economically required adjustments.

## Simplified emission runway

Let $A_{\mathrm{emission}}$ be assets or backing allocated to an emission policy and $C_e$ its estimated cost per epoch. A simplified runway estimate is:

$$\operatorname{Runway}_{\mathrm{epochs}} = \frac{A_{\mathrm{emission}}}{C_e}$$

If there are $E_d$ epochs per day:

$$\operatorname{Runway}_{\mathrm{days}} = \frac{A_{\mathrm{emission}}}{C_e E_d}$$

Real runway changes with treasury prices, supply, staking participation, reward rates, liabilities, and liquidity. It is a scenario estimate—not a countdown guarantee.

## Symbol reference

| Symbol | Meaning |
|---|---|
| $r_e$ | Reward yield for epoch $e$ |
| $R_e$ | PULSAR distributed in epoch $e$ |
| $S_e$ | Eligible staked PULSAR in epoch $e$ |
| $Q_e$ | QUASAR balance at epoch $e$ |
| $I_t$ | QUASAR index at time $t$ |
| $W$ | Wrapped QUASAR balance |
| $C_t$ | QUASAR represented per wrapped token |
| $V_i$ | Market value of treasury asset $i$ |
| $h_i$ | Approved valuation multiplier after haircut |
| $L$ | Counted treasury liabilities |
| $S_{\mathrm{circ}}$ | Circulating PULSAR supply |
| $\delta$ | Authorized distribution fraction |

