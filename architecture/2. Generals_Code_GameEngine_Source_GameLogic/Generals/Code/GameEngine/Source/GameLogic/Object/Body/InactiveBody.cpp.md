# Generals/Code/GameEngine/Source/GameLogic/Object/Body/InactiveBody.cpp

## Purpose
This file implements the `InactiveBody` class, which represents an inactive body module in the game engine. It handles damage and healing for objects that do not have a physical body.

## Responsibilities
- Manages damage and healing for inactive objects.
- Ensures that inactive objects cannot be affected by health-related events.
- Handles specific exceptions like unstoppable damage types.

## Key Types
- `InactiveBody` (Class): Represents an inactive body module with no health or damage capabilities.

## Key Functions
### InactiveBody::InactiveBody
- Purpose: Initializes the inactive body module and marks the object as effectively dead.
- Calls: 
  - `getObject()->setEffectivelyDead(true)`

### estimateDamage
- Purpose: Estimates the amount of damage an inactive body can take. Returns 0 unless the damage type is unstoppable.
- Calls: None

### attemptDamage
- Purpose: Attempts to apply damage to an inactive body. If the damage type is unstoppable, it triggers the object's death process.
- Calls:
  - `getObject()->onDie(damageInfo)`
  - `attemptHealing(damageInfo)`

### attemptHealing
- Purpose: Attempts to heal an inactive body. Returns no effect since inactive bodies cannot be healed.
- Calls:
  - `attemptDamage(damageInfo)`

### internalChangeHealth
- Purpose: Changes the health of an inactive body. Does nothing since inactive bodies have no health.

### getHealth
- Purpose: Retrieves the health of an inactive body, which is always 0.
- Calls: None

### getDamageState
- Purpose: Returns the damage state of an inactive body, which is always pristine.
- Calls: None

### setDamageState
- Purpose: Sets the damage state of an inactive body. Does nothing since inactive bodies cannot have their damage state changed.
- Calls: None

### crc
- Purpose: Computes the CRC for the inactive body module.
- Calls:
  - `BodyModule::crc(xfer)`

### xfer
- Purpose: Transfers data for the inactive body module.
- Calls:
  - `xfer->xferVersion(&version, currentVersion)`
  - `BodyModule::xfer(xfer)`

### loadPostProcess
- Purpose: Performs post-processing after loading an inactive body module.
- Calls:
  - `BodyModule::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/InactiveBody.h"
  - "GameLogic/Module/DieModule.h"
  - "GameLogic/Damage.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
