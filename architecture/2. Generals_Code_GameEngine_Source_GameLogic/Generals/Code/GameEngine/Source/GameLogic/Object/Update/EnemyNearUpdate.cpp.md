# Generals/Code/GameEngine/Source/GameLogic/Object/Update/EnemyNearUpdate.cpp

## Purpose
This file contains the implementation of the `EnemyNearUpdate` class, which handles enemy detection and updates for game objects in Command & Conquer Generals.

## Responsibilities
- Detects when an enemy is within range.
- Updates the object's state based on enemy presence.
- Manages a delay between enemy scans to prevent excessive checks.

## Key Types
- `EnemyNearUpdate` (Class): Handles enemy detection and updates for game objects.

## Key Functions
### checkForEnemies
- Purpose: Periodically checks for enemies within the object's vision range.
- Calls:
  - `getEnemyNearUpdateModuleData()->m_enemyScanDelayTime`
  - `getObject()->getVisionRange()`
  - `TheAI->findClosestEnemy`

### update
- Purpose: Updates the object's state based on enemy presence and changes its model condition accordingly.
- Calls:
  - `checkForEnemies`
  - `getDrawable()->setModelConditionState`
  - `getDrawable()->clearModelConditionState`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/PerfTimer.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/Module/EnemyNearUpdate.h"
  - "GameLogic/Object.h"
  - "GameLogic/AI.h"
  - "GameLogic/Module/AIUpdate.h"
