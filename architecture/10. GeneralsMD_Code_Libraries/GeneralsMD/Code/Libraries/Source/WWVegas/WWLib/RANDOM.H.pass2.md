# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RANDOM.H - Enhanced Analysis

## Architectural Role
This header defines the core random number generation utilities used throughout the SAGE engine. It provides multiple RNG implementations with different quality/speed tradeoffs, serving as the foundation for procedural generation, AI decision-making, and other stochastic behaviors in the game.

## Cross-References
### Incoming
- AI behavior systems (e.g., pathfinding, unit decisions)
- Game logic for procedural events (e.g., random map generation)
- Networking for simulating latency or randomizing multiplayer behaviors
- Particle effects and visual systems requiring randomness

### Outgoing
- No direct outgoing references (header-only, no implementation dependencies)

## Design Patterns
- **Template Method**: `Pick_Random_Number` uses a template to work with any RNG class, abstracting the random number generation logic.
- **Strategy Pattern**: Multiple RNG classes (`RandomClass`, `Random2Class`, etc.) implement different strategies for randomness, allowing the engine to choose based on needs (speed vs. quality).
- **Singleton-like Usage**: While not a true singleton, the RNG classes are designed to be instantiated once and reused, implying a "global" randomness state pattern.
