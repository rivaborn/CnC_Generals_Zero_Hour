# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialAbilityUpdate.h

## Purpose
Defines the `SpecialAbilityUpdate` module for handling unit special abilities in the game.

## Responsibilities
- Manages special ability execution (preparation, triggering, cleanup)
- Handles packing/unpacking of special objects
- Validates and tracks special objects
- Controls targeting and range checks

## Key Types
- **SpecialAbilityUpdateModuleData (Class)**: Configuration data for special abilities (ranges, timings, effects).
- **SpecialAbilityUpdate (Class)**: Core module implementing special ability logic.
- **PackingState (Enum)**: States for packing/unpacking process (NONE, PACKING, UNPACKING, PACKED, UNPACKED).

## Key Functions
### `initiateIntentToDoSpecialPower`
- Purpose: Initiates a special ability.
- Calls: Not inferable.

### `update`
- Purpose: Updates the special ability state.
- Calls: Not inferable.

### `approachTarget`
- Purpose: Moves the unit toward the target.
- Calls: Not inferable.

### `triggerAbilityEffect`
- Purpose: Executes the special ability's effect.
- Calls: Not inferable.

### `handlePackingProcessing`
- Purpose: Manages packing/unpacking of special objects.
- Calls: Not inferable.

## Globals
- **SPECIAL_ABILITY_HUGE_DISTANCE (const float)**: Large distance value for range checks.

## Dependencies
- `Common/AudioEventRTS.h`, `Common/INI.h`, `GameLogic/Module/SpecialPowerUpdateModule.h`, `GameClient/ParticleSys.h`
- `DamageInfo`, `SpecialPowerTemplate`, `SpecialPowerModule`, `FXList`, `SpecialPowerType` (forward declarations).
