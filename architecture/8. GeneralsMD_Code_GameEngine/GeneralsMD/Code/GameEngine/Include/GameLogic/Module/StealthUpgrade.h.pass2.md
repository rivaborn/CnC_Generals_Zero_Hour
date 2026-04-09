# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StealthUpgrade.h - Enhanced Analysis

## Architectural Role
This file defines a specialized upgrade module that grants stealth capability to game objects. It integrates into the game's upgrade system, modifying object behavior by setting the `OBJECT_STATUS_CAN_STEALTH` status flag.

## Cross-References
### Incoming
- Likely called by `UpgradeModule` subclasses or the upgrade system when applying stealth upgrades
- May be referenced in object templates or upgrade definitions in data files

### Outgoing
- Inherits from `UpgradeModule`, calling its constructor and implementing virtual methods
- Operates on `Thing` objects (game entities) to modify their status

## Design Patterns
- **Template Method Pattern**: Uses `upgradeImplementation()` as a hook for derived behavior
- **Module Pattern**: Encapsulates stealth upgrade logic as a self-contained module
- **Memory Pool Pattern**: Uses custom memory allocation for performance optimization

*Not inferable: No other patterns clearly visible in this header-only file.*
