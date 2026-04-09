# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SubObjectsUpgrade.h - Enhanced Analysis

## Architectural Role
This file defines a module within the upgrade system that dynamically controls subobject visibility based on upgrade states. It integrates with the W3D rendering pipeline by overriding animation-driven subobject states, enabling visual upgrades like weapon attachments or structural modifications.

## Cross-References
### Incoming
- **UpgradeModule.h**: Uses base class functionality
- **Thing.h**: Attaches to game objects
- **MultiIniFieldParse**: For configuration parsing
- **Memory pool system**: For object allocation

### Outgoing
- **W3D rendering system**: Modifies subobject visibility
- **UpgradeModule system**: Inherits and extends upgrade logic
- **Thing subsystem**: Applies changes to attached objects

## Design Patterns
- **Module Pattern**: Encapsulates upgrade behavior as a reusable component
- **Strategy Pattern**: `upgradeImplementation` provides interchangeable upgrade logic
- **Data-Driven Design**: Configuration via `SubObjectsUpgradeModuleData` enables modding
