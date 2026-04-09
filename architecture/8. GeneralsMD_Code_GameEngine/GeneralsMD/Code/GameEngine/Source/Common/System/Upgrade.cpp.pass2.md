# GeneralsMD/Code/GameEngine/Source/Common/System/Upgrade.cpp - Enhanced Analysis

## Architectural Role
This file is the core of the upgrade system, bridging game logic and UI. It manages upgrade templates, veterancy progression, and affordability checks, while also handling serialization and INI parsing for modding support.

## Cross-References
### Incoming
- `GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/*.cpp` (various upgrade implementations)
- `GeneralsMD/Code/GameEngine/Source/GameClient/InGameUI.cpp` (for UI feedback)
- `GeneralsMD/Code/GameEngine/Source/Common/Player.cpp` (for money checks)

### Outgoing
- `GeneralsMD/Code/GameEngine/Source/Common/Xfer.cpp` (serialization)
- `GeneralsMD/Code/GameEngine/Source/Common/INI.cpp` (INI parsing)
- `GeneralsMD/Code/GameEngine/Source/GameClient/Image.cpp` (button image handling)

## Design Patterns
- **Singleton**: `TheUpgradeCenter` as global access point
- **Factory Method**: `newUpgrade()` creates upgrade instances
- **Observer**: Upgrades notify UI via `TheInGameUI->message()` (implicit)

*Not inferable*: Template Method for upgrade behavior (likely in subclasses).
