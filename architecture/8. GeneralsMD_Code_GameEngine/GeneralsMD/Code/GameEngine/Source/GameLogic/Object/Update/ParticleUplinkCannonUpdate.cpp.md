# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ParticleUplinkCannonUpdate.cpp

## Purpose
Handles building states and weapon firing logic for the Particle Uplink Cannon special weapon.

## Responsibilities
- Manages cannon state transitions (idle, charging, firing, etc.)
- Controls visual effects (particles, lasers, flares)
- Handles damage application and scorch marks
- Manages audio events for cannon operations
- Supports manual targeting and scripted waypoint paths

## Key Types
- `ParticleUplinkCannonUpdateModuleData` (Struct): Configuration data for cannon behavior
- `ParticleUplinkCannonUpdate` (Class): Main update module handling cannon logic
- `PUCStatus` (Enum): Cannon state machine states
- `LaserStatus` (Enum): Laser beam states

## Key Functions
### `update()`
- Purpose: Main update loop for cannon state management
- Calls: `testStatus`, `setLogicalStatus`, `calculateUpBonePositions`, `createGroundToOrbitLaser`, `createOrbitToTargetLaser`, `createScorchMarks`, `createDamagePulseRemnants`, `createLaunchFX`, `removeAllEffects`

### `setLogicalStatus(PUCStatus)`
- Purpose: Handles state transitions and associated effects
- Calls: `clearModelConditionFlags`, `clearAndSetModelConditionFlags`, `removeAudioEvent`, `addAudioEvent`

### `setClientStatus(PUCStatus, Bool)`
- Purpose: Updates client-side visual effects for state changes
- Calls: `calculateDefaultInformation`, `removeAllEffects`, `createOuterNodeParticleSystems`, `createConnectorLasers`, `createConnectorFlare`, `createLaserBaseFlare`, `createGroundToOrbitLaser`

### `initiateIntentToDoSpecialPower()`
- Purpose: Initiates cannon activation with target positioning
- Calls: `getSpecialPowerModule`, `setReadyFrame`, `markSpecialPowerTriggered`

## Globals
- None

## Dependencies
- Common: `ThingTemplate`, `ThingFactory`, `Player`, `PlayerList`, `Xfer`, `ClientUpdateModule`
- GameClient: `ControlBar`, `GameClient`, `Drawable`, `ParticleSys`, `FXList`
- GameLogic: `GameLogic`, `PartitionManager`, `Object`, `ObjectIter`, `Weaponset`, `Weapon`, `TerrainLogic`, `SpecialPowerModule`, `PhysicsUpdate`, `LaserUpdate`, `ActiveBody`
- Audio: `TheAudio` (global audio system)
