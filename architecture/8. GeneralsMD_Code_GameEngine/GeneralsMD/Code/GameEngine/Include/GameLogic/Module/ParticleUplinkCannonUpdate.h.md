# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ParticleUplinkCannonUpdate.h

## Purpose
Defines the update module for the Particle Uplink Cannon's building states and weapon firing logic.

## Responsibilities
- Manages the cannon's state machine (charging, firing, etc.)
- Handles particle effects, lasers, and audio events
- Controls damage application and visual feedback
- Processes special power commands and target overrides

## Key Types
- **ParticleUplinkCannonUpdateModuleData (Class)**: Configuration data for the cannon's behavior and effects.
- **PUCStatus (Enum)**: Cannon state machine (IDLE, CHARGING, FIRING, etc.).
- **LaserStatus (Enum)**: Laser beam lifecycle states (BORN, DECAYING, etc.).
- **IntensityTypes (Enum)**: Effect intensity levels (LIGHT, MEDIUM, INTENSE).
- **ParticleUplinkCannonUpdate (Class)**: Core update module implementing SpecialPowerUpdateModule.

## Key Functions
### `initiateIntentToDoSpecialPower`
- Purpose: Initiates the special power action.
- Calls: Not inferable.

### `update`
- Purpose: Main update loop for state transitions and effects.
- Calls: Not inferable.

### `createOuterNodeParticleSystems`
- Purpose: Spawns particle effects on outer nodes.
- Calls: Not inferable.

### `createConnectorLasers`
- Purpose: Creates laser connectors between nodes.
- Calls: Not inferable.

### `removeAllEffects`
- Purpose: Cleans up all active effects.
- Calls: Not inferable.

## Globals
- **MAX_OUTER_NODES (const)**: Maximum number of outer nodes (16).

## Dependencies
- `SpecialPowerUpdateModule.h` (inheritance)
- `Common/KindOf.h`, `Common/Science.h` (includes)
- `SpecialPowerModule`, `ParticleSystem`, `FXList`, `AudioEventRTS` (forward references)
