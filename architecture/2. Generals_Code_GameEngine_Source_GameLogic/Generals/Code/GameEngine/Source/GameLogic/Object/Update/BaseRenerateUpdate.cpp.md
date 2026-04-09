# Generals/Code/GameEngine/Source/GameLogic/Object/Update/BaseRenerateUpdate.cpp

## Purpose
This file implements the `BaseRegenerateUpdate` module, which handles the automatic regeneration of health for base objects in Command & Conquer Generals.

## Responsibilities
- Manages health regeneration for base objects.
- Handles damage events to adjust regeneration behavior.
- Updates object health periodically based on configuration settings.

## Key Types
- **BaseRegenerateUpdateModuleData (struct):** Stores data for the base regenerate update module.
- **BaseRegenerateUpdate (class):** Implements the logic for base health regeneration.

## Key Functions
### BaseRegenerateUpdate::BaseRegenerateUpdate
- Purpose: Initializes the base regenerate update module.
- Calls: `setWakeFrame`

### BaseRegenerateUpdate::onDamage
- Purpose: Adjusts regeneration behavior based on damage received.
- Calls: `setWakeFrame`

### BaseRegenerateUpdate::update
- Purpose: Updates object health periodically if conditions are met.
- Calls: `attemptHealing`, `setWakeFrame`

## Globals
- **None**

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/GlobalData.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/BaseRegenerateUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Object.h"

- External symbols:
  - `TheGlobalData`
  - `UPDATE_SLEEP_FOREVER`
  - `UPDATE_SLEEP_NONE`
  - `LOGICFRAMES_PER_SECOND`
