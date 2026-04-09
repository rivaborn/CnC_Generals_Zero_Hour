# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GrantUpgradeCreate.h - Enhanced Analysis

## Architectural Role
This file defines a module in the game's component-based architecture that handles upgrade granting to objects. It extends the `CreateModule` base class, integrating into the game's object lifecycle system (creation/build completion) and the upgrade system.

## Cross-References
### Incoming
- Likely called by the game's object creation system (e.g., `Thing` factory or `CreateModule` manager)
- Used by modders via the module system (as indicated by `buildFieldParse`)

### Outgoing
- Calls into the upgrade system (not inferable which one)
- Uses `ObjectStatusTypes` for status checks
- Relies on `CreateModule` base class for lifecycle hooks

## Design Patterns
- **Template Method**: `onCreate`/`onBuildComplete` are virtual hooks for subclass behavior
- **Component Pattern**: Module attaches to `Thing` objects as a behavior extension
- **Data-Driven Design**: Module data parsed from config files (`buildFieldParse`)
