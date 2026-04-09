# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AI.cpp

## Purpose
Core AI system implementation for Command & Conquer Generals Zero Hour, handling game logic, pathfinding, and unit behavior.

## Responsibilities
- Manages AI data structures and configuration
- Handles pathfinding and unit grouping
- Implements target selection logic
- Processes AI updates per frame
- Manages AI-related game state serialization

## Key Types
- **TAiData (Class)**: Main AI configuration data container
- **AISideInfo (Class)**: Side-specific AI parameters
- **AISideBuildList (Class)**: Build list information per faction
- **PartitionFilterLiveMapEnemies (Class)**: Filter for live enemy objects on map
- **PartitionFilterWithinAttackRange (Class)**: Filter for objects within attack range
- **TPriorityInfo (Struct)**: Priority information for target selection

## Key Functions
### `findClosestEnemy`
- Purpose: Finds closest enemy target based on attack qualifiers
- Calls: `ThePartitionManager->getClosestObject`, `contain->iterateContained`, `priorityFunc`

### `findClosestAlly`
- Purpose: Finds closest ally target based on qualifiers
- Calls: `ThePartitionManager->getClosestObject`

### `getAdjustedVisionRangeForObject`
- Purpose: Calculates adjusted vision range considering various factors
- Calls: `object->getVisionRange`, `object->getLargestWeaponRange`

### `priorityFunc`
- Purpose: Callback for priority calculation during target selection
- Calls: `contain->iterateContained`

## Globals
- **TheAIFieldParseTable (FieldParse[])**: Configuration parsing table for AI data
- **TheAI (AI*)**: Global AI system singleton instance

## Dependencies
- PartitionManager.h (for spatial queries)
- AIUpdate.h (for AI module updates)
- ScriptEngine.h (for scripted attack info)
- Weapon.h (for weapon range calculations)
- Common game systems (Player, GameState, etc.)
