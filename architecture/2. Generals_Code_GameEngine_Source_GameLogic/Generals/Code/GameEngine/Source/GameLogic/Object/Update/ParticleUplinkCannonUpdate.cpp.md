# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ParticleUplinkCannonUpdate.cpp

## Purpose
Handles the update logic for the particle uplink cannon, including its state transitions, weapon firing, and visual effects.

## Responsibilities
- Manages the charging, preparing, and firing states of the particle uplink cannon.
- Updates visual effects such as particle systems and lasers.
- Handles sound events associated with different states.
- Processes user input for manual target control.

## Key Types
- **ParticleUplinkCannonUpdateModuleData (struct)**: Stores configuration data for the particle uplink cannon's update module.
- **ParticleUplinkCannonUpdate (class)**: Manages the state and behavior of the particle uplink cannon during gameplay.

## Key Functions
### ParticleUplinkCannonUpdate::update()
- Purpose: Updates the state and visual effects of the particle uplink cannon.
- Calls:
  - `killEverything()`
  - `setLogicalStatus()`
  - `setClientStatus()`

### ParticleUplinkCannonUpdate::initiateIntentToDoSpecialPower()
- Purpose: Initiates the special power sequence for the particle uplink cannon.
- Calls:
  - `setLogicalStatus()`
  - `markSpecialPowerTriggered()`

### ParticleUplinkCannonUpdate::calculateDefaultInformation()
- Purpose: Calculates default bone positions and orientations for visual effects.
- Calls:
  - `convertBonePosToWorldPos()`

## Globals
- None

## Dependencies
- **Common\ThingTemplate.h**
- **Common\ThingFactory.h**
- **Common\Player.h**
- **Common\PlayerList.h**
- **Common\Xfer.h**
- **GameClient\ControlBar.h**
- **GameClient\GameClient.h**
- **GameClient\Drawable.h**
- **GameClient\ParticleSys.h**
- **GameClient\FXList.h**
- **GameLogic\GameLogic.h**
- **GameLogic\PartitionManager.h**
- **GameLogic\Object.h**
- **GameLogic\ObjectIter.h**
- **GameLogic\Weaponset.h**
- **GameLogic\Weapon.h**
- **GameLogic\TerrainLogic.h**
- **GameLogic\Module\SpecialPowerModule.h**
- **GameLogic\Module\ParticleUplinkCannonUpdate.h**
- **GameLogic\Module\PhysicsUpdate.h**
- **GameLogic\Module\LaserUpdate.h**
- **GameLogic\Module\ActiveBody.h**
