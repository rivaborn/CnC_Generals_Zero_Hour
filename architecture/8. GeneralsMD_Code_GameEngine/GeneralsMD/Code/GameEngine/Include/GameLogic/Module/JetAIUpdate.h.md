# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/JetAIUpdate.h

## Purpose
Defines the JetAIUpdate module for aircraft AI behavior in the game.

## Responsibilities
- Manages jet-specific AI states (takeoff, landing, taxiing, combat).
- Handles locomotion, targeting, and special abilities (afterburners, lock-on).
- Tracks producer location and pending commands.
- Controls runway interactions and parking behavior.

## Key Types
- **JetAIUpdateModuleData (Class)**: Configuration data for jet AI behavior (damage, locomotion, sounds).
- **JetAIUpdate (Class)**: Core AI update interface for jets, managing movement, combat, and state transitions.
- **FlagType (Enum)**: Bit flags for jet state (e.g., takeoff in progress, landing in progress).
- **JetAIUpdateMagicEnum (Enum)**: Placeholder for unimplemented glue code.
- **HAS_PENDING_COMMAND, ALLOW_AIR_LOCO, etc. (Enum values)**: Specific flag types.

## Key Functions
### `update()`
- Purpose: Updates jet AI state each frame.
- Calls: `pruneDeadTargeters()`, `positionLockon()`, state machine methods.

### `aiDoCommand(const AICommandParms* parms)`
- Purpose: Executes AI commands (move, attack, enter, repair).
- Calls: `privateFollowPath()`, `privateEnter()`, `privateGetRepaired()`.

### `chooseLocomotorSet(LocomotorSetType wst)`
- Purpose: Selects locomotion set based on current state.
- Calls: None directly (logic internal).

### `getSneakyTargetingOffset(Coord3D* offset) const`
- Purpose: Calculates offset for "sneaky" targeting.
- Calls: None.

## Globals
- None.

## Dependencies
- `AIUpdate.h`, `AIStateMachine
