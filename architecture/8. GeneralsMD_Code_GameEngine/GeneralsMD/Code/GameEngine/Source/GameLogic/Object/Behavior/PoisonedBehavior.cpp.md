# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/PoisonedBehavior.cpp

## Purpose
Implements behavior for objects affected by poison damage, applying continuous damage over time.

## Responsibilities
- Applies periodic damage to poisoned objects
- Manages poison duration and visual effects
- Handles healing to remove poison state
- Tracks poison damage timing and amounts

## Key Types
- **PoisonedBehaviorModuleData (struct)**: Stores poison damage interval and duration settings
- **PoisonedBehavior (class)**: Manages poison behavior logic and effects

## Key Functions
### `onDamage`
- Purpose: Initiates poison effects when poison damage is received
- Calls: `startPoisonedEffects`

### `onHealing`
- Purpose: Removes poison effects when healing occurs
- Calls: `stopPoisonedEffects`, `setWakeFrame`

### `update`
- Purpose: Handles periodic poison damage and effect management
- Calls: `getPoisonedBehaviorModuleData`, `TheGameLogic->getFrame`, `getObject()->attemptDamage`, `stopPoisonedEffects`, `calcSleepTime`

### `startPoisonedEffects`
- Purpose: Activates poison visual effects and damage timer
- Calls: `getPoisonedBehaviorModuleData`, `TheGameLogic->getFrame`, `getObject()->getDrawable`, `setWakeFrame`

### `stopPoisonedEffects`
- Purpose: Deactivates poison visual effects and timers
- Calls: `getObject()->getDrawable`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/Module/PoisonedBehavior.h`, `GameLogic/Damage.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`
