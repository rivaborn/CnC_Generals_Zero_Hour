# Generals/Code/Libraries/Source/WWVegas/WWLib/rng.h - Enhanced Analysis

## Architectural Role
This file defines the core abstraction for random number generation in the SAGE engine, serving as a foundational utility for stochastic behavior across game systems (AI, unit behavior, procedural effects). Its minimalist design allows for different RNG implementations while maintaining consistency in the interface.

## Cross-References
### Incoming
- `Generals/Code/Libraries/Source/WWVegas/WWLib/rndstrng.h` (uses `Get_Block` for string generation)
- Likely game logic files (AI, unit behavior) for random decision-making

### Outgoing
- None (pure interface, no dependencies)

## Design Patterns
- **Abstract Factory**: The interface enables runtime selection of RNG implementations.
- **Dependency Inversion**: High-level modules depend on this abstraction rather than concrete RNGs.
- **Not inferable**: No other patterns evident from the interface alone.
