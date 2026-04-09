# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotagePowerPlantCrateCollide.cpp

## Purpose
Handles collision logic for sabotage crates that disable enemy power plants.

## Responsibilities
- Validates target power plants for sabotage
- Triggers power plant sabotage effects
- Manages sabotage duration and player notifications
- Handles serialization and network transfer

## Key Types
- **SabotagePowerPlantCrateCollide (Class)**: Manages power plant sabotage behavior
- **SabotagePowerPlantCrateCollideModuleData (Not inferable)**: Contains sabotage parameters

## Key Functions
### `isValidToExecute`
- Purpose: Checks if target is valid for sabotage
- Calls: `CrateCollide::isValidToExecute`, `isEffectivelyDead`, `isKindOf`, `getRelationship`

### `executeCrateBehavior`
- Purpose: Executes sabotage on valid target
- Calls: `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `TheEva->setShouldPlay`, `getEnergy()->setPowerSabotagedTillFrame`, `onPowerBrownOutChange`

### `crc`
- Purpose: Serialization checksum
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Network serialization
- Calls: `CrateCollide::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- None

## Dependencies
- Common: `GameAudio`, `MiscAudio`, `Player`, `PlayerList`, `Radar`, `ThingTemplate`, `Xfer`
- GameClient: `Drawable`, `Eva`, `InGameUI`
- GameLogic: `ExperienceTracker`, `AIUpdate`,
