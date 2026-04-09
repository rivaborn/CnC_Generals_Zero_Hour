# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpawnBehavior.h

## Purpose
Defines the SpawnBehavior module, which manages spawning and monitoring of slave units, replacing them as needed.

## Responsibilities
- Spawn and monitor slave units
- Handle slave unit deaths and replacements
- Propagate damage and orders to slaves
- Manage spawning behavior via configuration

## Key Types
- **SpawnBehaviorModuleData (Class)**: Holds configuration for spawning behavior (template names, counts, delays, etc.)
- **SpawnBehaviorInterface (Class)**: Interface for interacting with spawned units (attack orders, status queries)
- **SpawnBehavior (Class)**: Core module implementing spawning logic and interface
- **CanAttackResult (Enum)**: Result of attack capability checks
- **SpawnBehaviorMagicEnum (Enum)**: Not inferable (placeholder)

## Key Functions
### `update()`
- Purpose: Update spawning logic periodically
- Calls: `shouldTryToSpawn()`, `createSpawn()`, `computeAggregateStates()`

### `onSpawnDeath(ObjectID deadSpawn, DamageInfo *damageInfo)`
- Purpose: Handle death of spawned units
- Calls: `reclaimOrphanSpawn()`

### `orderSlavesToAttackTarget(Object *target, Int maxShotsToFire, CommandSourceType cmdSource)`
- Purpose: Order slaves to attack a target
- Calls: Not inferable (external)

### `computeAggregateStates()`
- Purpose: Calculate aggregate states (e.g., health) from slaves
- Calls: Not inferable (internal)

## Globals
- **SPAWN_UPDATE_RATE (Int)**: Update frequency for spawning logic (half a second)

## Dependencies
- `BehaviorModule.h`, `UpdateModule.h`, `DieModule.h`, `DamageModule.h`
- `Common/INI.h` for configuration parsing
- `ThingTemplate`, `DamageInfo`, `ObjectID` types
