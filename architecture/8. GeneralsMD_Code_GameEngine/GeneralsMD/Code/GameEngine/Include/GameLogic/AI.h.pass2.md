# GeneralsMD/Code/GameEngine/Include/GameLogic/AI.h - Enhanced Analysis

## Architectural Role
This header defines the core AI subsystem, serving as the central interface for group management, command execution, and pathfinding. It bridges the game logic layer with the object system and pathfinding infrastructure, enabling both scripted and dynamic AI behaviors.

## Cross-References
### Incoming
- **TurretAI.h**: Uses AI group interfaces for turret targeting and behavior
- **GameLogic/Object.h**: Likely references AI commands for object behavior
- **Networking subsystems**: Probably calls AI interfaces for synchronized command execution

### Outgoing
- **Common/Snapshot.h**: Inherits for save/load functionality
- **GameLogic/Damage.h**: Uses damage types for AI decision-making
- **Pathfinder subsystem**: Called for movement and attack path calculations

## Design Patterns
- **Singleton**: `TheAI` provides global AI subsystem access
- **Command Pattern**: `AICommandParms` encapsulates command parameters
- **Composite**: `AIGroup` manages collections of objects as a single unit

*Not inferable*: Exact implementation of pathfinding delegation or event handling.
