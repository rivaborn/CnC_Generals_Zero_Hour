# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rng.h - Enhanced Analysis

## Architectural Role
This file defines the core abstraction for random number generation in the SAGE engine, serving as a foundational utility for game logic, AI decision-making, and procedural content generation. Its minimalist design allows for different RNG implementations to be swapped without affecting dependent systems.

## Cross-References
### Incoming
- `rndstrng.h` (likely uses this interface for string-based randomization)
- AI systems (for probabilistic behavior)
- Game logic (for random events/outcomes)

### Outgoing
- None (pure interface, no dependencies)

## Design Patterns
- **Interface Segregation**: Minimal interface with only essential functionality (`Get_Block`)
- **Dependency Inversion**: Allows concrete RNG implementations to be injected into systems needing randomness
- **Not inferable**: No other patterns clearly visible in this header-only file

*Token count: 150*
