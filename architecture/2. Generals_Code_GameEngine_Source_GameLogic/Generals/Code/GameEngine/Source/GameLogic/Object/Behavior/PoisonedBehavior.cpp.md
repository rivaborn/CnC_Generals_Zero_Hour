# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/PoisonedBehavior.cpp

## Purpose
This file implements the `PoisonedBehavior` class, which handles the effects of poison damage on game objects. It manages continuous damage over time and visual effects.

## Responsibilities
- React to poison damage by applying continuous damage.
- Manage the duration and interval of poison effects.
- Update visual effects (tinting) for poisoned objects.
- Handle healing to stop poison effects.

## Key Types
- `PoisonedBehaviorModuleData` (struct): Stores data about poison intervals and durations.
- `PoisonedBehavior` (class): Manages the behavior of a poisoned object.

## Key Functions
### startPoisonedEffects
- Purpose: Starts the poisoned effects on an object after receiving poison damage.
- Calls:
  - `getObject()->attemptDamage`
  - `Drawable::setTintStatus`

### stopPoisonedEffects
- Purpose: Stops the poisoned effects and resets related states.
- Calls:
  - `Drawable::clearTintStatus`

### update
- Purpose: Updates the poisoned state, applying damage at intervals and checking if effects should end.
- Calls:
  - `getObject()->attemptDamage`
  - `calcSleepTime`

### calcSleepTime
- Purpose: Calculates the sleep time for the module based on current poison frames.
- Calls:
  - `frameToSleepTime`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/Module/PoisonedBehavior.h"
  - "GameLogic/Damage.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"

- External symbols used:
  - `TheGameLogic`
  - `TINT_STATUS_POISONED`
  - `DAMAGE_POISON`
  - `DAMAGE_UNRESISTABLE`
  - `DEATH_POISONED`
  - `INVALID_ID`
