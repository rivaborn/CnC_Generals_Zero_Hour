# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/AutoHealBehavior.cpp

## Purpose
This file implements the `AutoHealBehavior` class, which manages auto-healing functionality for game objects in Command & Conquer Generals.

## Responsibilities
- Manages auto-healing behavior for game objects.
- Handles particle systems for visual effects.
- Iterates over nearby objects to apply healing.
- Responds to damage events to reset the healing process.

## Key Types
- **AutoHealPlayerScanHelper (Class)**: Helper struct used in iterating over player-owned objects to find those eligible for healing.

## Key Functions
### checkForAutoHeal
- Purpose: Checks if an object is eligible for auto-healing and adds it to a list.
- Calls: None

### AutoHealBehavior::AutoHealBehavior
- Purpose: Constructor initializes the behavior, sets up particle systems, and determines initial activation state.
- Calls: `createParticleSystem`, `setPosition`, `setWakeFrame`

### AutoHealBehavior::~AutoHealBehavior
- Purpose: Destructor cleans up particle systems.
- Calls: `destroyParticleSystemByID`

### AutoHealBehavior::stopHealing
- Purpose: Stops the healing process.
- Calls: None

### AutoHealBehavior::undoUpgrade
- Purpose: Resets the upgrade state and wake frame.
- Calls: None

### AutoHealBehavior::onDamage
- Purpose: Handles damage events to reset the healing process if conditions are met.
- Calls: `setWakeFrame`

### AutoHealBehavior::update
- Purpose: Main update function that applies healing to eligible objects.
- Calls: `iterateObjects`, `pulseHealObject`, `createParticleSystem`, `setPosition`, `addWorldAnimation`

### AutoHealBehavior::pulseHealObject
- Purpose: Applies healing to a single object and creates a particle system effect.
- Calls: `attemptHealing`, `attemptHealingFromSoleBenefactor`, `createParticleSystem`, `setPosition`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Thing.h"
  - "Common/ThingTemplate.h"
  - "Common/INI.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameClient/ParticleSys.h"
  - "GameClient/Anim2D.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/Module/AutoHealBehavior.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"

- External symbols used:
  - `TheParticleSystemManager`
  - `TheGameLogic`
  - `TheAnim2DCollection`
  - `TheGlobalData`
