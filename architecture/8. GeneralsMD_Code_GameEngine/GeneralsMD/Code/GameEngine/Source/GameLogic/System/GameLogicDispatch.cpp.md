# GeneralsMD/Code/GameEngine/Source/GameLogic/System/GameLogicDispatch.cpp

## Purpose
Handles game logic message dispatching and command processing for the SAGE engine in Command & Conquer Generals/Zero Hour.

## Responsibilities
- Processes game messages and dispatches commands to appropriate objects
- Manages movement and rally point commands
- Handles beacon placement/removal and text setting
- Manages game state transitions (new game, clearing game data)
- Processes team creation/selection commands

## Key Types
- `GameLogic` (Class): Main game logic controller
- `AIGroup` (Class): Group of AI-controlled objects
- `Object` (Class): Game world object base class
- `GameMessage` (Class): Message container for game commands
- `Player` (Class): Player representation

## Key Functions
### `doMoveTo`
- Purpose: Issues movement command to an object
- Calls: `ai->queueWaypoint`, `ai->clearWaypointQueue`, `obj->leaveGroup`, `ai->aiMoveToPosition`

### `doSetRallyPoint`
- Purpose: Sets rally point for production objects after path validation
- Calls: `TheAI->pathfinder()->clientSafeQuickDoesPathExist`, `TheInGameUI->message`, `exitInterface->setRallyPoint`

### `logicMessageDispatcher`
- Purpose: Main message processing function that routes commands
- Calls: `TheAI->createGroup`, `thisPlayer->getCurrentSelectionAsAIGroup`, `TheStatsCollector->collectMsgStats`, various player-specific message handlers

### `prepareNewGame`
- Purpose: Initializes game state for new game
- Calls: `TheScriptEngine->setGlobalDifficulty`, `TheGameLogic->setGameMode`, `TheShell->hideShell`

### `clearGameData`
- Purpose: Cleans up game state when ending a game
- Calls: `TheStatsCollector->writeFileEnd`, `TheGameEngine->reset`, `TheShell->push`

## Globals
- `theBuildPlan` (Bool): Tracks if build planning mode is active
- `thePlanSubject` (Object*): Array of objects in build plan
- `thePlanSubjectCount` (int): Count of objects in build plan

## Dependencies
- Key includes: `GameLogic.h`, `AI.h`, `Player.h`, `MessageStream.h`, `Recorder.h`
- External symbols: `TheAI`, `TheGameLogic`, `ThePlayerList`, `TheInGameUI`, `TheAudio`, `TheRadar`, `TheControlBar`, `TheWindowManager`, `TheShell`, `TheTacticalView`, `TheLookAtTranslator`, `TheMouse`, `TheStatsCollector`, `TheNetwork`, `TheRecorder`, `TheGlobalData`, `TheWritableGlobalData`, `TheNameKeyGenerator`, `TheThingFactory`, `TheLocomotorStore`, `TheScriptEngine`, `TheScriptActions`, `TheVictoryConditions`, `TheEva`, `TheMultiplayerSettings`, `TheTransitionHandler`, `TheParticleSys`, `TheGameText`, `TheGameEngine`, `TheParticleSysManager`, `TheParticleSysStore`, `TheParticleSysFactory`, `TheParticleSysTemplateStore`, `TheParticleSysTemplateFactory`, `TheParticleSysTemplateManager`
