# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/SpawnBehavior.cpp

## Purpose
This file implements the `SpawnBehavior` class, which manages the spawning and behavior of units in a game. It handles creating, monitoring, and replacing spawned units based on various conditions.

## Responsibilities
- Manage the creation and lifecycle of spawned units.
- Handle unit replacements when existing units die.
- Aggregate health and veterancy levels from spawned units to the spawner.
- Distribute selection states among spawned units and the spawner.
- Control spawning behavior based on game logic and conditions.

## Key Types
- **OrphanData (Class)**: Manages orphaned data related to spawned units.

## Key Functions
### SpawnBehavior::SpawnBehavior
- Purpose: Initializes the spawn behavior with module data.
- Calls: `TheThingFactory->findTemplate`, `m_replacementTimes.clear`.

### SpawnBehavior::~SpawnBehavior
- Purpose: Cleans up resources when the spawn behavior is destroyed.
- Calls: `m_replacementTimes.clear`.

### SpawnBehavior::onDelete
- Purpose: Destroys spawned units if they are not already dead.
- Calls: `TheGameLogic->destroyObject`, `TheGameLogic->findObjectByID`.

### SpawnBehavior::onDie
- Purpose: Handles the death of the spawner, including notifying spawned units and destroying them if necessary.
- Calls: `SlavedUpdateInterface::onSlaverDie`, `TheGameLogic->kill`, `TheGameLogic->destroyObject`.

### SpawnBehavior::update
- Purpose: Updates the spawn behavior every frame, managing spawning and replacement logic.
- Calls: `computeAggregateStates`, `createSpawn`, `m_replacementTimes.erase`.

### SpawnBehavior::maySpawnSelfTaskAI
- Purpose: Determines if spawned units can perform self-tasking AI based on certain conditions.
- Calls: `getObject->getAI`, `AIUpdateInterface::getLastCommandSource`.

### SpawnBehavior::getClosestSlave
- Purpose: Finds the closest spawned unit to a given position.
- Calls: `ThePartitionManager->getDistanceSquared`.

### SpawnBehavior::orderSlavesToAttackTarget
- Purpose: Orders all spawned units to attack a specific target.
- Calls: `AIUpdateInterface::aiForceAttackObject`.

### SpawnBehavior::orderSlavesToGoIdle
- Purpose: Orders all spawned units to go idle.
- Calls: `AIUpdateInterface::aiIdle`.

### SpawnBehavior::getCanAnySlavesAttackSpecificTarget
- Purpose: Checks if any spawned unit can attack a specific target.
- Calls: `Object::getAbleToAttackSpecificObject`.

### SpawnBehavior::createSpawn
- Purpose: Creates a new spawned unit and initializes it.
- Calls: `TheThingFactory->spawn`, `exitInterface->reserveDoorForExit`, `exitInterface->exitObjectViaDoor`.

### SpawnBehavior::onSpawnDeath
- Purpose: Handles the death of a spawned unit, including scheduling replacements.
- Calls: `m_replacementTimes.push_back`, `TheGameLogic->destroyObject`.

### SpawnBehavior::stopSpawning
- Purpose: Stops the spawning process.

### SpawnBehavior::startSpawning
- Purpose: Starts the spawning process.

### SpawnBehavior::onDamage
- Purpose: Notifies spawned units of damage to the spawner.
- Calls: `SlavedUpdateInterface::onSlaverDamage`.

### SpawnBehavior::shouldTryToSpawn
- Purpose: Determines if the spawner should attempt to spawn new units based on conditions.
- Calls: `getObject->getStatusBits`, `getObject->testStatus`.

### SpawnBehavior::computeAggregateStates
- Purpose: Aggregates various states (health, veterancy) from spawned units to the spawner.
- Calls: `Object::getExperienceTracker`, `BodyModuleInterface::getHealth`, `Drawable::isSelected`.

## Globals
- None

##
