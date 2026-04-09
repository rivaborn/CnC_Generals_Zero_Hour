# GeneralsMD/Code/GameEngine/Include/Common/ClientUpdateModule.h - Enhanced Analysis

## Architectural Role
This file defines the abstract base class for client-side update modules, bridging the game's module system with client-specific logic. It enforces a pure virtual `clientUpdate()` method, ensuring derived classes implement client-side behavior while inheriting from `DrawableModule`.

## Cross-References
### Incoming
- Likely called by the game loop or client update manager (e.g., `GameClient.cpp` or `ClientUpdateManager.h`)
- Used by derived modules (e.g., `UnitModule.h`, `BuildingModule.h`) for client-side updates

### Outgoing
- Inherits from `DrawableModule`, implying dependency on rendering/update systems
- Uses `ModuleData` for configuration, linking to the module system

## Design Patterns
- **Template Method**: `clientUpdate()` is a pure virtual method, forcing subclasses to implement client-specific logic while the update mechanism is standardized.
- **Inheritance Hierarchy**: Extends `DrawableModule`, indicating a clear separation between server and client update logic.
- **Interface Segregation**: The `getModuleType()` and `getInterfaceMask()` methods suggest a modular architecture where modules are identified by type and interface flags.

Not inferable: No other patterns are explicitly visible in this header.
