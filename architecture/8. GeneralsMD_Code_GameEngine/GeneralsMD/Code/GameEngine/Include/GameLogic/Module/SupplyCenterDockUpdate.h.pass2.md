# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyCenterDockUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the supply center's economic logic, bridging cargo management and player resource systems. It implements the `DockUpdate` pattern for periodic resource conversion, with tight coupling to the INI-based module system.

## Cross-References
### Incoming
- **GameLogic/Module/DockUpdate.h**: Base class inheritance and interface implementation
- **Common/INI.h**: Module data configuration parsing
- **GameLogic/Thing.h** (implied): `Thing` parameter in constructor

### Outgoing
- **GameLogic/Object.h**: `Object` parameters in `action()` and `update()`
- **GameLogic/Player.h** (implied): Money grant operations
- **GameLogic/Cargo.h** (implied): Cargo-to-money conversion logic

## Design Patterns
- **Module Pattern**: Encapsulates supply center behavior as a pluggable module
- **Strategy Pattern**: `DockUpdate` interface allows different dock behaviors
- **Memory Pool Pattern**: Uses `MEMORY_POOL_GLUE` for object allocation optimization
