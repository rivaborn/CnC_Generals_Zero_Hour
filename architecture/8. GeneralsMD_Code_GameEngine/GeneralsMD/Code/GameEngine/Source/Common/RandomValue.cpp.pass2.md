# GeneralsMD/Code/GameEngine/Source/Common/RandomValue.cpp - Enhanced Analysis

## Architectural Role
This file implements the core pseudo-random number generation system, critical for game logic determinism and client-side effects. It enforces separation between game logic (deterministic) and client/audio (non-deterministic) random streams, ensuring replayability while allowing visual variation.

## Cross-References
### Incoming
- Game logic systems (e.g., AI, unit behavior) call `GetGameLogicRandomValue`/`Real` for deterministic decisions
- Client rendering systems use `GetGameClientRandomValue`/`Real` for visual effects
- Audio systems call `GetGameAudioRandomValueReal` for sound variation

### Outgoing
- Directly manipulates seed arrays (`theGameLogicSeed`, `theGameClientSeed`, `theGameAudioSeed`)
- Uses `TheGameLogic` global for frame logging (debug builds only)
- Relies on `CRC.h` for seed hashing in `GetGameLogicRandomSeedCRC`

## Design Patterns
- **Separated Interface**: Client/logic/audio have distinct random streams to maintain determinism
- **Factory Method**: `GameClientRandomVariable`/`GameLogicRandomVariable` encapsulate distribution logic
- **Singleton-like**: Global seed arrays act as implicit singletons for random state

*Not inferable*: Exact usage of `DistributionType` variants (GAUSSIAN/TRIANGULAR) appears unimplemented.
