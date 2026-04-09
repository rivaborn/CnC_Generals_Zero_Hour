# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate.cpp

## Purpose
This file implements generic AI mechanisms for game objects, including state management, pathfinding, and command handling.

## Responsibilities
- Manage AI states and transitions.
- Handle pathfinding requests and updates.
- Process commands from players and other sources.
- Update object positions and behaviors based on AI logic.

## Key Types
- **AIUpdateModuleData (Struct)**: Stores data for AI modules, including turret configurations and locomotor templates.
- **TurretAIData (Class)**: Manages AI data specific to turrets.
- **LocomotorTemplateVector (Typedef)**: Vector of locomotor templates.

## Key Functions
### AIUpdateModuleData::findLocomotorTemplateVector
- Purpose: Retrieve a vector of locomotor templates based on the locomotor set type.
- Calls: `m_locomotorTemplates.find`

### AIUpdateInterface::setGoalPositionClipped
- Purpose: Set the goal position for an object, ensuring it stays within map boundaries.
- Calls: `TheTerrainLogic->getExtent`, `getStateMachine()->setGoalPosition`

### AIUpdateInterface::doPathfind
- Purpose: Perform pathfinding operations using the PathfindServicesInterface.
- Calls: `pathfinder->updateGoal`, `pathfinder->updatePos`

## Globals
- None

## Dependencies
- **Includes**:
  - "Common/ActionManager.h"
  - "GameLogic/AI.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Object.h"
  - "GameLogic/ScriptEngine.h"
  - "GameClient/ControlBar.h"
  - "GameClient/Drawable.h"
  - "Common/Xfer.h"
- **External Symbols**:
  - `TheLocomotorStore`
  - `TheTerrainLogic`
  - `TheAI`
  - `TheAudio`
  - `TheScriptEngine`
  - `TheControlBar`
