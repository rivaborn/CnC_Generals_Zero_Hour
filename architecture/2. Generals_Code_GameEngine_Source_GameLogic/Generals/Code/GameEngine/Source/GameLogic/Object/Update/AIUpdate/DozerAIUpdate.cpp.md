# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/DozerAIUpdate.cpp

## Purpose
This file implements the AI behavior for Dozers in Command & Conquer Generals, handling tasks like building, repairing, and moving.

## Responsibilities
- Manages Dozer tasks such as building, repairing, and fortifying.
- Implements state machines for different actions (picking position, moving to position, performing action).
- Handles AI commands and updates the Dozer's state accordingly.

## Key Types
- **DozerPrimaryStateMachine (Class)**: Manages primary states like idle, build, repair, etc.
- **DozerActionStateMachine (Class)**: Manages specific actions within tasks.
- **DozerActionType (Enum)**: Defines types of actions (pick position, move to position, do action).
- **DozerActionPickActionPosState (Class)**: State for picking a position around the target.
- **DozerActionMoveToActionPosState (Class)**: State for moving to the picked position.
- **DozerActionDoActionState (Class)**: State for performing the actual action.

## Key Functions
### findObjectToRepair
- Purpose: Finds an object to repair.
- Calls: `TheGameLogic->findObjectByID`, `getTaskTarget`.

### findMine
- Purpose: Finds a mine.
- Calls: `ThePartitionManager->findPositionAround`.

## Globals
- **MIN_ACTION_TOLERANCE (Real)**: Minimum tolerance for action distance.

## Dependencies
- Key includes:
  - "Common/ActionManager.h"
  - "Common/Team.h"
  - "Common/StateMachine.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Locomotor.h"
  - "GameClient/Drawable.h"
  - "GameLogic/Module/CreateModule.h"
  - "GameLogic/Module/DozerAIUpdate.h"
