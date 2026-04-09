# Generals/Code/GameEngine/Source/GameLogic/System/GameLogicDispatch.cpp

## Purpose
Handles game logic message dispatching, including movement commands and rally point setting.

## Responsibilities
- Dispatches object command messages to appropriate objects.
- Manages game state transitions like starting new games and clearing game data.
- Processes various game messages such as movement, beacon placement, and team management.

## Key Types
- None

## Key Functions
### doMoveTo
- Purpose: Issues a move command to an object.
- Calls: `queueWaypoint`, `clearWaypointQueue`, `leaveGroup`, `releaseWeaponLock`, `aiMoveToPosition`

### doSetRallyPoint
- Purpose: Sets a rally point for an object, with path validation.
- Calls: `quickDoesPathExist`, `message`, `addAudioEvent`, `setRallyPoint`

### getSingleObjectFromSelection
- Purpose: Retrieves a single object from the current selection group.
- Calls: `getAllIDs`, `findObjectByID`

## Globals
- `theBuildPlan` (Bool): Indicates if a build plan is active.
- `thePlanSubject` (Object*[]): Array of objects in the build plan.
- `thePlanSubjectCount` (int): Count of objects in the build plan.

## Dependencies
- Key includes: "PreRTS.h", "Common/CRCDebug.h", "GameLogic/AIPathfind.h", "GameLogic/GameLogic.h", "GameClient/InGameUI.h", etc.
- External symbols: `TheAI`, `TheGameLogic`, `ThePlayerList`, `TheNetwork`, `TheRecorder`, etc.
