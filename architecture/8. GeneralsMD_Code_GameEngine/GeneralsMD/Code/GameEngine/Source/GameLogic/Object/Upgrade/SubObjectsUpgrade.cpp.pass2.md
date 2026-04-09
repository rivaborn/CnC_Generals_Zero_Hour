# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/SubObjectsUpgrade.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized upgrade module that dynamically controls subobject visibility in W3D models based on upgrade states. It bridges the game logic layer with the rendering system by modifying Drawable components, enabling visual upgrades like weapon attachments or structural modifications.

## Cross-References
### Incoming
- **Upgrade System**: Other upgrade modules likely instantiate or query this module
- **INI Parser**: Called during module initialization to parse configuration
- **Network Code**: Uses CRC/xfer for synchronization across clients

### Outgoing
- **Drawable System**: Directly manipulates subobject visibility via `showSubObject()`
- **Upgrade Framework**: Inherits from `UpgradeModule` and uses its base methods
- **Object System**: Accesses object properties through `getObject()`

## Design Patterns
- **Template Method**: Extends `UpgradeModule` with `upgradeImplementation()` as the core hook
- **Strategy**: Encapsulates subobject visibility logic as a modular upgrade behavior
- **Observer**: Reacts to upgrade state changes to trigger visual updates (implicit via upgrade system)

*Not inferable*: No clear use of Factory, Decorator, or Visitor patterns in this snippet.
