# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/POWTruckAIUpdate.cpp

## Purpose
This file contains the implementation of AI logic for POW trucks in Command & Conquer Generals. It handles tasks such as picking up prisoners, returning them to prisons, and managing the truck's state.

## Responsibilities
- Manage POW truck tasks including waiting, finding targets, collecting prisoners, and returning prisoners.
- Handle AI commands from players or other sources.
- Update the POW truck's state based on current tasks and conditions.
- Ensure proper containment of prisoners within the truck and unloading them into prisons.

## Key Types
- **POWTruckAIUpdateModuleData (struct)**: Stores configuration data for POW truck AI, such as bored time and prison distance.
- **POWTruckAIUpdate (class)**: Implements the AI logic for POW trucks, managing tasks and state transitions.

## Key Functions
### POWTruckAIUpdate::aiDoCommand
- Purpose: Handles AI commands for the POW truck.
- Calls:
  - `privatePickUpPrisoner`
  - `privateReturnPrisoners`

### POWTruckAIUpdate::update
- Purpose: Updates the POW truck's state and performs actions based on the current task.
- Calls:
  - `updateWaiting`
  - `updateFindTarget`
  - `updateCollectingTarget`
  - `updateReturnPrisoners`

### POWTruckAIUpdate::privatePickUpPrisoner
- Purpose: Initiates the process of picking up a prisoner.
- Calls:
  - `setTask`
  - `aiMoveToObject`

### POWTruckAIUpdate::privateReturnPrisoners
- Purpose: Initiates the process of returning prisoners to a prison.
- Calls:
  - `findBestPrison`
  - `setTask`
  - `aiDock`

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/ActionManager.h"
  - "Common/GlobalData.h"
  - "Common/Money.h"
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/OpenContain.h"
  - "GameLogic/Module/POWTruckAIUpdate.h"

- **External Symbols**:
  - `TheGameLogic`
  - `TheActionManager`
  - `TheGlobalData`
  - `ThePartitionManager`
  - `TheAI`
  - `TheInGameUI`
