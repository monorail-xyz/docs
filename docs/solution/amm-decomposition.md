# AMM Decomposition

## Decompose AMM Curves

AMM curves define continuous price functions, making them fundamentally different from orderbook structures. Monorail's approach begins by decomposing these curves into a new liquidity model.

For each AMM, the algorithm:

- Analyzes how liquidity and pricing change across different trade sizes
- Builds a comprehensive map of available liquidity
- Models price impact behavior throughout the new model

### Protocol Agnostic Design

This transformation method works with any AMM that can provide quotes, ensuring the model remains viable as AMM designs evolve. This flexibility makes it future-proof against new implementations.

### Key Features

- Creates a single, coherent view of executable liquidity
- Maintains mathematical rigor necessary for optimal execution
- Preserves each venue's unique advantages

### Previous Implementation Experience

This builds on previous work the Monorail team did to deploy Curve-style concentrated AMM liquidity to orderbooks:

- [Astroport Injective Orderbook Integration](https://github.com/astroport-fi/astroport-core/tree/main/contracts/pair_concentrated_inj)
- [Astroport Neutron Orderbook Integration](https://github.com/astroport-fi/astroport-core/tree/feat/duality-integration/contracts/pair_concentrated_duality)
