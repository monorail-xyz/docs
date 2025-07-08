# Trade Routing

## Trade Execution

Monorail's execution algorithm analyzes available liquidity across all venues, starting from the best available price. The process:

1. Walks through aggregated liquidity level by level
2. Determines optimal order size for each venue
3. Creates precise venue-by-venue breakdown
4. Executes atomically through our aggregation contract

This ensures trades capture the best available liquidity while minimizing price impact.

## Direct Pairs (Single-hop Trades)

For direct trading pairs:

- Applies liquidity aggregation to determine optimal venue split
- Uses unified liquidity curve for best execution
- Considers all sources simultaneously

## Indirect Pairs (Multi-hop Trades)

For complex trades:

- Extends optimization across all viable paths between input/output tokens
- Optimizes each leg individually using the unified model
- Considers complete liquidity landscape at each step
- Finds best pricing across multiple hops

## Dynamic Slippage Protection

!!! note "Not available yet"

    This feature is not yet available on testnet

Traditional aggregators and AMMs typically require traders to set fixed slippage tolerance values, often leading to either failed transactions or excessive slippage.

Monorail's sophisticated approach:

- Understands complete liquidity landscape around optimal execution point
- Dynamically calculates precise slippage tolerances
- Uses actual market depth for calculations
- Results in better execution guarantees
- Reduces failed trades
