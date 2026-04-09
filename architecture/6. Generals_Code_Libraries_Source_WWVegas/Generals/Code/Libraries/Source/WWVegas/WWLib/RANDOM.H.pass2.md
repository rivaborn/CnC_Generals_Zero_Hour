# Generals/Code/Libraries/Source/WWVegas/WWLib/RANDOM.H - Enhanced Analysis

## Architectural Role
This header defines the core random number generation utilities used throughout the engine. It provides multiple RNG implementations with different quality/speed tradeoffs, serving as the foundation for procedural generation, AI decision-making, and other stochastic behaviors.

## Cross-References
### Incoming
- AI behavior systems (e.g., unit pathfinding, tactical decisions)
- Game logic (e.g., random events, loot generation)
- Rendering effects (e.g., particle systems, weather)
- Networking (e.g., desync mitigation via deterministic RNG seeding)

### Outgoing
- None (header-only, no external dependencies)

## Design Patterns
- **Strategy Pattern**: Multiple RNG implementations (RandomClass, Random2Class, etc.) can be swapped based on requirements.
- **Template Method**: `Pick_Random_Number` uses a template to work with any RNG class.
- **Singleton-like Usage**: RNG instances are typically created once and reused (implied by static-like usage in comments).

**Note**: The file includes warnings about dimensional bias in Random2Class and Random3Class, indicating real-world usage constraints.
