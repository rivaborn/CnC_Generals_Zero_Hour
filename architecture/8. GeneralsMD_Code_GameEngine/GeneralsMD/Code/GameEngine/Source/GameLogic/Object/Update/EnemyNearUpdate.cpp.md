# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/EnemyNearUpdate.cpp

## Purpose
Handles detection and reaction when an enemy enters the vision range of a game object.

## Responsibilities
- Periodically scans for nearby enemies
- Updates object's visual state when enemy is detected/lost
- Manages cooldown between scans
- Serializes module state for network sync

## Key Types
- **EnemyNearUpdate (Class)**: Module that monitors enemy proximity and triggers visual changes
- **EnemyNearUpdateModuleData (Not shown)**: Configuration data for scan delays/ranges

## Key Functions
### `checkForEnemies()`
- Purpose: Scans for closest enemy within vision range
- Calls: `TheAI->findClosestEnemy()`

### `update()`
- Purpose: Main update loop that checks enemies and updates visual states
- Calls: `checkForEnemies()`, `getObject()->getDrawable()->setModelConditionState()`

### `xfer()`
- Purpose: Serializes module state for network synchronization
- Calls: `UpdateModule::xfer()`

## Globals
- **TheAI (AI**) : Global AI instance for enemy detection

## Dependencies
- `UpdateModule.h`, `ThingTemplate.h`, `Drawable.h`, `AI.h`
- `MODELCONDITION_ENEMYNEAR` (enum), `GameLogicRandomValue()` (function)
