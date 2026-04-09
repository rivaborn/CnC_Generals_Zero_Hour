# GeneralsMD/Code/GameEngine/Include/Common/GameType.h - Enhanced Analysis

## Architectural Role
This header defines foundational enums and constants that serve as the type system backbone for the SAGE engine. It bridges the core engine (pathfinding, rendering) with game logic (units, formations) by providing shared identifiers and game state categories.

## Cross-References
### Incoming
- Game logic files (Unit.cpp, Building.cpp) use ObjectID/DrawableID for entity management
- AI system (Pathfinder.cpp) references PathfindLayerEnum for navigation layers
- W3D rendering uses DrawableID for scene graph management
- UI/HUD systems reference FormationID for tactical display

### Outgoing
- Relies on BaseType.h for primitive type definitions
- Forward-declares INI class for configuration loading
- TimeOfDay/Weather enums drive environmental effects in W3D and Audio systems

## Design Patterns
- **Type Object Pattern**: Enums like ObjectID act as handles for runtime object lookup
- **Enumerated Constants**: TimeOfDay/Weather use named constants for configuration
- **Layered Architecture**: PathfindLayerEnum implements a layered system for pathfinding

*Not inferable*: No class-based patterns visible in header-only file.
