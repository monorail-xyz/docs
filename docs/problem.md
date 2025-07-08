# The Problem

While existing chains have forced users to rely primarily on AMMs due to high gas costs and slow block times, Monad's performance improvements enable true on-chain orderbooks to operate alongside AMMs for the first time.

## Market Structure Analysis

| Feature                      | Orderbooks             | AMMs                           |
| ---------------------------- | ---------------------- | ------------------------------ |
| Long-tail assets             | Requires market making | Passive                        |
| Precise pricing              | Yes                    | Depends on model and liquidity |
| Less slippage / price impact | Dependent on depth     | Deterministic                  |
| Constant liquidity           | Active management      | Automatic                      |

## Core Technical Challenges

### Structure Mismatch

- AMMs define liquid markets through continuous mathematical functions (e.g., x\*y=k constant product curves)
- Traditional orderbooks operate with discrete limit orders at specific prices
- These fundamentally different expressions of liquidity must be normalized for comparison

### Dynamic Efficiency Trade-offs

- Orderbooks excel at price discovery and typically offer minimal slippage for trades within their liquidity depth
- AMMs guarantee always-available liquidity but with deterministic price impact
- The optimal mix between these venues varies based on market conditions and trade size

### Execution Complexity

- Each venue type has different execution costs and gas requirements
- Price impact calculations differ between AMMs and orderbooks
- Route optimization must consider both immediate price impact and gas costs
- Splitting orders across venues requires careful size optimization

Monorail has created an innovative [solution](solution/index.md) to this problem, and for the first time, enables the integration of AMMs and orderbooks into a unified trading experience.
