# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CleanupAreaPower.cpp - Enhanced Analysis

## Architectural Role
This file implements the cleanup power system for units like ambulances, bridging the gap between special power activation and hazard cleanup mechanics. It extends the `SpecialPowerModule` base class to handle cleanup-specific logic and coordinates with the `CleanupHazardUpdate` module.

## Cross-References
### Incoming
- **SpecialPowerModule subclasses**: Likely called by unit-specific power implementations (e.g., ambulance) when cleanup is triggered.
- **INI parsing system**: Invokes `buildFieldParse` during module initialization to configure cleanup parameters.

### Outgoing
- **CleanupHazardUpdate**: Delegates cleanup execution via `setCleanupAreaParameters`.
- **SpecialPowerModule**: Inherits core functionality (serialization, state management).
- **Object system**: Uses `findUpdateModule` to locate cleanup-related updates.

## Design Patterns
- **Template Method**: Extends `SpecialPowerModule` with cleanup-specific implementations (e.g., `doSpecialPowerAtLocation`).
- **Dependency Injection**: Receives `CleanupAreaPowerModuleData` via constructor, decoupling configuration from logic.
- **Command Pattern**: Encapsulates cleanup behavior as a reusable module, invoked by higher-level power systems.
