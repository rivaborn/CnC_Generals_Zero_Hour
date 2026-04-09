# Generals/Code/GameEngine/Source/GameLogic/Object/Update/NeutronMissileUpdate.cpp

## Purpose
This file implements the behavior of a neutron missile in the game, including its launch, attack, and collision handling.

## Responsibilities
- Manage the lifecycle of a neutron missile.
- Handle missile launch and targeting.
- Update missile position and orientation during flight.
- Process collisions and detonation effects.

## Key Types
- **NeutronMissileUpdateModuleData (struct)**: Stores configuration data for the missile's behavior.
- **NeutronMissileUpdate (class)**: Manages the missile's state and updates its position and orientation.

## Key Functions
### projectileLaunchAtObjectOrPosition
- Purpose: Prepares the missile for launch by setting initial parameters.
- Calls: `projectileFireAtObjectOrPosition`

### projectileFireAtObjectOrPosition
- Purpose: Initiates the missile's launch sequence.
- Calls: None

### doLaunch
- Purpose: Handles the missile's launch state, including position and orientation updates.
- Calls: `calcTransform`, `FXList::doFXObj`, `TheParticleSystemManager->createAttachedParticleSystemID`

### calcTransform
- Purpose: Calculates the transformation matrix for the missile to orient towards its target.
- Calls: None

### doAttack
- Purpose: Handles the missile's attack state, including movement and collision checks.
- Calls: `calcTransform`, `getObject()->getDrawable()->setInstanceMatrix`

### projectileHandleCollision
- Purpose: Processes collisions with other objects during flight.
- Calls: `detonate`

### detonate
- Purpose: Triggers the missile's explosion effects and marks it as dead.
- Calls: None

## Globals
- **STRAIGHT_DOWN_SLOW_FACTOR (Real)**: Factor to slow down the missile when moving straight down.

## Dependencies
- Key includes:
  - "Common/GameState.h"
  - "Common/Thing.h"
  - "GameLogic/Object.h"
  - "GameClient/FXList.h"
  - "GameClient/ParticleSys.h"
