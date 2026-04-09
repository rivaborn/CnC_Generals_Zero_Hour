# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/SubdualDamageHelper.cpp - Enhanced Analysis

## Architectural Role
This file implements a helper class for managing subdual damage healing, bridging the gap between the BodyModule's damage system and the game's update loop. It ensures subdual damage is gradually removed over time without requiring BodyModule to handle periodic updates directly.

## Cross-References
### Incoming
- **BodyModule**: Calls `notifySubdualDamage` when subdual damage is applied
- **Game Loop**: Invokes `update` during object processing

### Outgoing
- **BodyModuleInterface**: Uses `getSubdualDamageHealRate`, `getSubdualDamageHealAmount`, `hasAnySubdualDamage`, and `attemptDamage`
- **ObjectHelper**: Inherits and calls base class methods (`crc`, `xfer`, `loadPostProcess`)

## Design Patterns
- **Observer Pattern**: `notifySubdualDamage` acts as a callback for damage events
- **State Machine**: Uses `UpdateSleepTime` to control update frequency based on healing state
- **Helper Pattern**: Encapsulates auxiliary logic for BodyModule, following SAGE's modular design

*Not inferable*: No clear use of Strategy or Command patterns in this snippet.
