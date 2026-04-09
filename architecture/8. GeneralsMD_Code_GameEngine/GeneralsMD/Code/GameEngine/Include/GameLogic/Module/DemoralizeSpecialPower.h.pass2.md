# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DemoralizeSpecialPower.h - Enhanced Analysis

## Architectural Role
This file defines the demoralize special power module, a key component of the game's special abilities system. It extends the base `SpecialPowerModule` to implement demoralization effects that scale with captured prisoners, demonstrating the engine's modular power system design.

## Cross-References
### Incoming
- `SpecialPowerModule` subclasses (e.g., `PlayerTemplate`) instantiate this module via the engine's power system.
- INI parsing infrastructure calls `buildFieldParse` during module initialization.

### Outgoing
- Calls into `SpecialPowerModule` base class for core power functionality.
- References `FXList` for visual/audio effects, indicating tight coupling with the effects system.
- Uses `MultiIniFieldParse` for configuration, showing dependency on the game's data-driven architecture.

## Design Patterns
- **Module Pattern**: The file implements a specialized module within the game's power system, following the engine's component-based design.
- **Data-Driven Design**: Configuration is externalized via INI parsing, allowing modders to tweak demoralize parameters without code changes.
- **Template Method**: `doSpecialPowerAtObject`/`doSpecialPowerAtLocation` suggest a template method pattern where base class defines the interface and derived class implements behavior.
