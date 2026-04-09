# GeneralsMD/Code/GameEngine/Include/Common/RandomValue.h - Enhanced Analysis

## Architectural Role
This header defines the core random number generation interface used across the engine, serving as the foundation for deterministic behavior in game logic, AI, and replay systems. It abstracts the RNG initialization and seed management, ensuring consistency across different subsystems.

## Cross-References
### Incoming
- `GameLogic/LogicRandomValue.h` (uses `GetGameLogicRandomSeed`/`GetGameLogicRandomSeedCRC`)
- `GameClient/ClientRandomValue.h` (uses `InitRandom`)
- `Common/AudioRandomValue.h` (uses `InitRandom`)

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Dependency Injection**: Subsystems provide their own RNG implementations (e.g., `LogicRandomValue.h`, `ClientRandomValue.h`) while relying on this header for seed management.
- **Facade Pattern**: Hides underlying RNG complexity behind simple initialization and seed access functions.
- **Singleton-like Behavior**: Global RNG state is managed via functions (`InitRandom`, `InitGameLogicRandom`), implying a single RNG instance per subsystem.

*Not inferable*: No clear use of Observer, Factory, or other patterns in this header.
