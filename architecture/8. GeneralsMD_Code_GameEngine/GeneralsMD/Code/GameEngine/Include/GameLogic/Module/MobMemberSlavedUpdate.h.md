# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MobMemberSlavedUpdate.h

## Purpose
Defines the `MobMemberSlavedUpdate` module for managing AI behavior of mob members (e.g., scout drones, stinger soldiers) that follow a master unit.

## Responsibilities
- Manages slaved unit behavior (following, attacking, catch-up logic).
- Handles state transitions (idle, catching up, attacking).
- Implements distance-based catch-up mechanics with teleport fallback.
- Controls visual effects for slaved/unslaved states.
- Parses INI configuration for mob behavior parameters.

## Key Types
- **MobMemberSlavedUpdateModuleData (Class)**: Holds INI-configurable parameters (catch-up radii, squirreliness ratio, bail time).
- **MobStates (Enum)**: Defines mob states (none, idle, catch-up, attacking).
- **MobMemberSlavedUpdate (Class)**: Core module implementing slaved update logic.
- **DamageInfo (Class)**: External type for damage notifications.
- **ModelConditionFlagType (Enum)**: External type for model conditions.

## Key Functions
### `doCatchUpLogic`
- Purpose: Adjusts unit position to stay within range of the master.
- Calls: Not inferable (implementation in .cpp).

### `update`
- Purpose: Main update loop for state transitions and behavior.
- Calls: Not inferable (implementation in .cpp).

### `onEnslave` / `onSlaverDie` / `onSlaverDamage`
- Purpose: Handles slaver lifecycle events (enslavement, death, damage).
- Calls: Not inferable (implementation in .cpp).

### `startSlavedEffects` / `stopSlavedEffects`
- Purpose: Toggles visual/audio effects for slaved state.
- Calls: Not inferable (implementation in .cpp).

## Globals
-
