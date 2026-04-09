# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SalvageCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the salvage crate collision behavior, a key part of the game's progression system. It bridges the collision detection system with player progression mechanics, handling reward distribution and eligibility checks.

## Cross-References
### Incoming
- **GameLogic/Module/SalvageCrateCollide.h**: Base class and module data definitions
- **Common/Kindof.h**: Unit type classification
- **GameLogic/ExperienceTracker.h**: Veterancy level management
- **GameClient/InGameUI.h**: Floating text notifications
- **Common/AudioEventRTS.h**: Sound event handling

### Outgoing
- **CrateCollide**: Base class collision behavior
- **Object**: Unit template and state management
- **Player**: Money and score tracking
- **TheAudio**: Sound event playback
- **TheInGameUI**: Visual feedback rendering

## Design Patterns
- **Strategy Pattern**: Different reward types (weapon/armor upgrades, money, levels) are handled by separate methods, allowing for easy extension.
- **Template Method**: `executeCrateBehavior` orchestrates the reward selection process, delegating to specific methods for each reward type.
- **State Pattern**: Unit upgrades modify internal state flags (e.g., `WEAPONSET_CRATEUPGRADE_ONE`), which are checked for eligibility.
