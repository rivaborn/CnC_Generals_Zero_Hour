# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/MobMemberSlavedUpdate.cpp

## Purpose
Handles AI behavior for "mob member" units that follow a master unit (e.g., angry mob members).

## Responsibilities
- Manages unit positioning relative to master
- Handles catch-up logic when unit strays too far
- Controls unit targeting and movement states
- Manages visual effects and selection state
- Handles master unit death/damage events

## Key Types
- `MobMemberSlavedUpdate` (Class): Main module controlling slaved unit behavior
- `MobStates` (Enum): Tracks unit state (e.g., catching up, idle)
- `MobMemberSlavedUpdateModuleData` (Struct): Configuration data for module

## Key Functions
### `update()`
- Purpose: Main update loop for slaved unit behavior
- Calls: `stopSlavedEffects()`, `getAIUpdateInterface()`, `aiMoveToPosition()`, `aiAttackObject()`, `maySpawnSelfTaskAI()`

### `doCatchUpLogic()`
- Purpose: Handles logic when unit needs to catch up to master
- Calls: `aiMoveToPosition()`, `setMobState()`

### `startSlavedEffects()`
- Purpose: Initializes effects when unit becomes slaved
- Calls: None

### `stopSlavedEffects()`
- Purpose: Cleans up effects when unit is no longer slaved
- Calls: None

## Globals
- `CLOSE_ENOUGH` (Real): Minimum distance threshold (15)
- `CLOSE_ENOUGH_SQR` (Real): Squared distance threshold
- `STRAY_MULTIPLIER` (Real): Multiplier for stray distance calculation

## Dependencies
- GameLogic headers (Object, AIUpdate, Locomotor)
- GameClient headers (Drawable, InGameUI)
- Common headers (RandomValue, Xfer)
- PartitionManager, TerrainLogic
- Module-specific headers (MobMemberSlavedUpdate, SpawnBehavior)
