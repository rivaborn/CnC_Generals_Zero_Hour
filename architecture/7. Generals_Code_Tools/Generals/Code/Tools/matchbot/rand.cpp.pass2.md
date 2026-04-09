# Generals/Code/Tools/matchbot/rand.cpp - Enhanced Analysis

## Architectural Role
This file implements a standalone PRNG utility used by matchbot tools (likely for AI behavior testing or scenario generation). It's isolated from the main game engine's PRNG (which may use a different algorithm for determinism in networking).

## Cross-References
### Incoming
- Likely called by matchbot tools (e.g., scenario generators, AI test harnesses) - not referenced in main game code.

### Outgoing
- None (fully self-contained, no external dependencies beyond `<cmath>`).

## Design Patterns
- **State Pattern**: The PRNG maintains internal state (seed array) that evolves with each call.
- **Factory Method**: `Int()` and `Double()` act as factory methods for different random number types.
- **Template Method**: The `randomValue()` core algorithm is a template for derived random number generation methods.

*Not inferable*: No clear use of Observer, Strategy, or other patterns. The ADC macro suggests low-level bit manipulation typical of early 2000s PRNGs.
