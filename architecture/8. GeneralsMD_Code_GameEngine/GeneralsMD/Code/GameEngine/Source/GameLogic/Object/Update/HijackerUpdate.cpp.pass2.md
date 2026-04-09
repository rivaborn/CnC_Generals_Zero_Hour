# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HijackerUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the core logic for the hijacker unit's vehicle interaction system, bridging the game's AI, physics, and object management subsystems. It handles state transitions between hijacked and free states, experience sharing, and special cases like airborne vehicle ejection.

## Cross-References
### Incoming
- **AIUpdate.h**: Uses `AIUpdateInterface` for idle behavior after vehicle ejection
- **ContainModule.h**: Interacts with container system for parachute spawning
- **ExperienceTracker.h**: Manages experience transfer between hijacker and vehicle
- **PartitionManager.h**: Registers/unregisters objects during state changes

### Outgoing
- **GameLogic.h**: Uses `TheGameLogic` for object lookup
- **ThingFactory.h**: Creates new objects (parachutes) during ejection
- **Drawable.h**: Controls visibility during hijacking
- **Object.h**: Manages object positions and status flags

## Design Patterns
- **State Pattern**: Manages hijacker's state transitions (in/out of vehicle)
- **Observer Pattern**: Tracks target vehicle state via ID reference
- **Dependency Injection**: Receives module data through constructor

*Not inferable*: Exact serialization pattern (Xfer) implementation details.
