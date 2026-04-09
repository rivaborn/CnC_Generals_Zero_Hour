# GeneralsMD/Code/GameEngine/Include/GameClient/Module/BeaconClientUpdate.h

## Purpose
Defines the BeaconClientUpdate module for handling beacon-related client updates in the game.

## Responsibilities
- Manages beacon visibility and radar pulses
- Handles particle system for beacon display
- Provides client-side update logic for beacons
- Configures beacon behavior via module data

## Key Types
- **BeaconClientUpdateModuleData (Class)**: Stores beacon configuration (frames between pulses, pulse duration).
- **BeaconClientUpdate (Class)**: Implements beacon client update logic.
- **BeaconClientUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **Thing (Class)**: Forward reference to game object.
- **ParticleSystem (Class)**: Forward reference to particle effects.

## Key Functions
### BeaconClientUpdate::clientUpdate
- Purpose: Handles periodic beacon updates (radar pulses).
- Calls: Not inferable (implementation in .cpp).

### BeaconClientUpdate::hideBeacon
- Purpose: Hides the beacon particle system.
- Calls: Not inferable.

### BeaconClientUpdateModuleData::buildFieldParse
- Purpose: Parses beacon module data from configuration files.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `ClientUpdateModule.h` (base class)
- `Thing` (forward reference)
- `ParticleSystem` (forward reference)
- `MultiIniFieldParse` (for config parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
