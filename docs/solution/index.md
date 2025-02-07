# Solution Overview

!!! note "Notice"

    This technical design overview is intended to be high-level. A more detailed document will be published as we progress through the
    development and refining the model

AMMs and orderbooks are typically seen as separate systems to trade on, introducing inefficiencies and complexity. Monorail takes a fundamentally different approach by transforming both market structures into a single, unified mathematical representation of liquidity.

## Core Innovation

The core innovation lies in Monorail's liquidity decomposition method: rather than trying to adapt orderbook mechanics to continuous AMM curves, Monorail decomposes AMM liquidity functions into a model that can be directly compared to orderbooks.

This creates a normalized representation that:

- Preserves the precise price discovery of orderbooks
- Maintains the continuous liquidity guarantees of AMMs
- Enables true aggregation rather than just cross-venue routing
- Allows direct mathematical comparison of liquidity at each price point

This approach eliminates the boundary between AMMs and orderbooks, allowing Monorail to optimize trades across all venues as if they were a single, deep source of liquidity.
