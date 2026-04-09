# GeneralsMD/Code/GameEngine/Include/Common/GameEngine.h - Enhanced Analysis

## Architectural Role
This header defines the central `GameEngine` class, acting as the root of the SAGE engine's architecture. It coordinates initialization, execution, and subsystem factories, serving as the primary interface between the game and its underlying systems.

## Cross-References
### Incoming
- `GameMain` (entry point) likely calls `CreateGameEngine` and `TheGameEngine->execute()`
- Subsystems (e.g., `AudioManager`, `GameLogic`) are instantiated via factory methods here
- UI/rendering systems likely query `m_isActive` for focus state

### Outgoing
- Calls into `FileSystem`, `NetworkInterface`, and other subsystems via factory methods
- Delegates game logic to `GameLogic` and rendering to `GameClient`
- Uses `MessageStream` for inter-process communication

## Design Patterns
- **Factory Method**: Abstracts creation of subsystems (e.g., `createGameLogic`), enabling runtime polymorphism
- **Singleton**: `TheGameEngine` provides global access to the engine instance
- **Facade**: Encapsulates complex subsystem interactions behind a unified interface

*Not inferable: Specific usage of `FunctionLexicon` or `ParticleSystemManager`.*
