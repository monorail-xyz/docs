# Unified Model

## Mathematical Framework

The algorith results in a single mathematical model that combines both AMM and orderbook liquidity.

### Total Liquidity Function

Given the price p, we define the total available liquidity as:

$$
L_{total}(p) = L_{amm}(p) + L_{ob}(p)
$$

### AMM Component

For AMMs, the liquidity function is defined as:

$$
L_{amm}(p) = \sum_i f_i(x, y, p)
$$

Where:

- $f_i$ represents the different AMM types (e.g., constant product, constant sum)
- $x$, $y$ represent the token reserves and pool state
- $p$ is the price level being evaluated

### Orderbook Component

For orderbooks, the liquidity function is:

$$
L_{ob}(p) = \sum_i v_i \quad \text{where} \quad p_i ≤ p
$$

Where:

- $v_i$ is the depth available at price level
- $p$ is the current price

## Advantages

This unified approach provides two key benefits:

1. More efficient price discovery by considering all available liquidity simultaneously
2. Reduced negative effects of market fragmentation by creating a single, deep liquidity pool
