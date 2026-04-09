# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/SpawnBehavior.cpp

## Purpose
Manages spawning and monitoring of units from a spawner object, handling replacement, health aggregation, and slave control.

## Responsibilities
- Spawns units based on templates and timing rules
- Manages spawned unit lifecycle (creation, death, replacement)
- Aggregates health/veterancy from spawned units
- Controls spawned units (attack orders, selection sync)
- Handles spawner death/damage propagation

## Key Types
- **SpawnBehavior (Class)**: Manages spawning behavior for objects
- **OrphanData (Class)**: Tracks orphaned spawned units (lines 518-530)
- **findClosestOrphan (Function)**: Finds nearest orphaned unit (lines 546-568)

## Key Functions
### `update`
- Purpose: Main update loop for spawning logic
- Calls: `computeAggregateStates`, `shouldTryToSpawn`, `createSpawn`, `stopSpawning`

### `onDie`
- Purpose: Handles spawner death and notifies spawned units
- Calls: `findObjectByID`, `getSlavedUpdateInterface`, `onSlaverDie`, `kill`

### `computeAggregateStates`
- Purpose: Calculates aggregate health/veterancy/selection for spawner
- Calls: `getExperienceTracker`, `getVeterancyLevel`, `setVeterancyLevel`, `getDrawable`, `isSelected`, `selectDrawable`

### `orderSlavesToAttackTarget`
- Purpose: Orders all spawned units to attack a target
- Calls: `findObjectByID`, `getAI`, `aiForceAttackObject`

## Globals
- **SPAWN_DELAY_MIN_FRAMES (const int)**: Minimum frames between spawns (16)
- **NONE_SPAWNED_YET (const uint32_t)**: Flag for unspawned state (0xffffffff)

## Dependencies
- **Common**: GameState, ThingFactory, ThingTemplate, Player, Xfer
- **GameLogic**: GameLogic, Object, PartitionManager, AIUpdate, SpawnBehavior, BodyModule, ExperienceTracker, StealthUpdate
- **GameClient**: Drawable, InGameUI
- **STL**: list, vector, iterator templates
