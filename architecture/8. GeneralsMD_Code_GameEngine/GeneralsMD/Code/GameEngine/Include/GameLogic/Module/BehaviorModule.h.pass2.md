# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BehaviorModule.h - Enhanced Analysis

## Architectural Role
This file defines the core behavior module interface hierarchy, serving as a central abstraction layer for game entity behaviors in the SAGE engine. It bridges between the game logic system and specific behavior implementations (e.g., parking, transport, special powers).

## Cross-References
### Incoming
- Game entity classes (e.g., Thing-derived objects) use this interface to access behavior functionality
- AI system components query behavior interfaces for decision-making
- Networking code uses serialization methods (crc/xfer) for synchronization

### Outgoing
- References multiple module interfaces (BodyModule, CollideModule, etc.) as dependencies
- Uses Common/Module.h for base class functionality
- Interacts with Team class for team-related behaviors

## Design Patterns
- **Interface Segregation**: Multiple small interfaces (ParkingPlaceBehaviorInterface, etc.) instead of one large interface
- **Dependency Injection**: BehaviorModule takes Thing and ModuleData in constructor
- **Strategy Pattern**: Different behavior implementations can be swapped via interface methods

*Not inferable: Concrete implementations of behavior interfaces not visible in header*
