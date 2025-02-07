# Introduction

The coming launch of Monad's high-throughput chain creates an opportunity: for the first time, both automated market makers (AMMs) and traditional orderbooks can operate efficiently on-chain. However, this introduces a new challenge - with 10+ AMMs and 3+ on-chain orderbooks already announced, liquidity will be heavily fragmented across venues with fundamentally different market structures.

## Overview

Monorail addresses this challenge by introducing a novel aggregation model that unifies these distinct liquidity sources. The approach combines:

- Precise price discovery and minimal slippage of orderbooks
- Broad token coverage and passive market making of AMMs
- Single, cohesive trading framework

This technical overview explains how Monorail's mathematical model transforms continuous AMM curves and discrete orderbook levels into a unified liquidity representation, enabling optimal trade execution across all venues while maintaining the unique advantages of each market structure.
