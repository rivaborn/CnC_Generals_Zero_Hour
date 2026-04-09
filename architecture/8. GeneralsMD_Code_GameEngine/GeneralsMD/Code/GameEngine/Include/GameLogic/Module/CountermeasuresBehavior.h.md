# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CountermeasuresBehavior.h

## Purpose
Defines the countermeasures behavior module for handling missile threats and flare deployment in the game.

## Responsibilities
- Manages countermeasure deployment (flares) to divert missiles
- Tracks missile threats and countermeasure availability
- Handles upgrade logic for countermeasure systems
- Provides interface for reporting missiles and calculating diversions

## Key Types
- **CountermeasuresBehaviorModuleData (Class)**: Configuration data for countermeasure behavior
- **CountermeasuresBehaviorInterface (Class)**: Virtual interface for countermeasure operations
- **CountermeasuresBehavior (Class)**: Main behavior module implementing countermeasure logic
- **CountermeasuresVec (Class)**: Vector of ObjectID for tracking countermeasures

## Key Functions
### CountermeasuresBehaviorModuleData::buildFieldParse
- Purpose: Defines INI field parsing for module data
- Calls: UpdateModuleData::buildFieldParse, UpgradeMuxData::getFieldParse

### CountermeasuresBehavior::update
- Purpose: Updates countermeasure state each frame
- Calls: Not inferable

### CountermeasuresBehavior::reportMissileForCountermeasures
- Purpose: Registers a missile threat for countermeasure response
- Calls: Not inferable

### CountermeasuresBehavior::calculateCountermeasureToDivertTo
- Purpose: Determines which countermeasure should divert a missile
- Calls: Not inferable

## Globals
- None

## Dependencies
- GameClient/ParticleSys.h
- GameLogic/Module/BehaviorModule.h
- GameLogic/Module/UpgradeModule.h
- GameLogic/Module/UpdateModule.h
- GameLogic/Module/DamageModule.h
- Common/BitFlagsIO.h
