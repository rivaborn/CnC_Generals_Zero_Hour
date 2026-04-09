# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CleanupAreaPower.h - Enhanced Analysis

## Architectural Role
This file defines a specialized power module that dynamically extends cleanup range until all hazards are removed, fitting into the engine's modular power system. It inherits from `SpecialPowerModule`, indicating it's part of the game's special ability framework.

## Cross-References
### Incoming
- Likely called by power management systems (e.g., `SpecialPowerManager`) when activating cleanup abilities
- Used by INI parsing infrastructure (`MultiIniFieldParse`) for module configuration

### Outgoing
- Inherits from `SpecialPowerModule`, using its base functionality
- Operates on `Thing` objects (likely game entities) for cleanup targeting
- Uses `Coord3D` for spatial calculations

## Design Patterns
- **Template Method**: Extends `SpecialPowerModule` with specific behavior in `doSpecialPowerAtLocation`
- **Module Pattern**: Encapsulates cleanup logic as a self-contained module
- **Memory Pool**: Uses `MEMORY_POOL_GLUE` for object allocation optimization (common in SAGE engine)
