# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/CommandXlat.cpp

## Purpose
Handles translation of raw input events into tactical commands and game messages.

## Responsibilities
- Processes game messages and translates them into actions
- Manages unit voice responses and sound playback
- Handles debug/demo commands and toggles
- Validates attack capabilities for selected units
- Manages command center location and hero status

## Key Types
- **DROPPED_MAX_PARTICLE_COUNT (Enum)**: Maximum particle count threshold
- **CommandCenterLocator (Class)**: Locates command centers or expensive buildings
- **HeroHolder (Class)**: Tracks hero unit status
- **CanAttackResult (Enum)**: Result of attack capability checks (Not inferable)
- **PickAndPlayInfo (Struct)**: Information for voice response playback (Not inferable)

## Key Functions
### `canSelectionSalvage`
- Purpose: Checks if selected units can salvage a target object
- Calls: `isSalvageCrate()`, `getAllSelectedDrawables()`, `isKindOf(KINDOF_SALVAGER)`

### `canObjectForceAttack`
- Purpose: Determines if an object can force attack a victim or position
- Calls: `isAbleToAttack()`, `getAbleToAttackSpecificObject()`, `getAbleToUseWeaponAgainstTarget()`, `getSpawnBehaviorInterface()`, `getClosestSlave()`, `getContain()`, `getClosestRider()`

### `pickAndPlayUnitVoiceResponse`
- Purpose: Plays appropriate voice responses for selected units based on message type
- Calls: `getObject()`, `isKindOf(KINDOF_IGNORED_IN_GUI)`, `getTemplate()`, `getPerUnitSound()`, `getVoiceSelect()`, `getVoiceMove()`, `getVoiceCrush()`, etc.

### `findCommandCenterOrMostExpensiveBuilding`
- Purpose: Locates the nearest command center or most expensive building
- Calls: `getPlayer()`, `getObject()`, `getTemplate()`, `getCost()`, `getPosition()`, `getDistanceToPoint()`

### `isSystemMessage`
- Purpose: Checks if a message is a system message that should not be displayed to the player
- Calls: `getType()`

## Globals
- **TheSkateDistOverride (Real)**: Debug override for skate distance (debug builds only)
- **DROPPED_MAX_PARTICLE_COUNT (Enum)**: Maximum particle count threshold

## Dependencies
- Key includes: `PreRTS.h`, `Common/AudioAffect.h`, `Common/ActionManager.h`, `Common/GameAudio.h`, `Common/GameEngine.h`, `Common/GameType.h`, `Common/GlobalData.h`, `Common/MessageStream.h`, `Common/MiscAudio.h`, `Common/MultiplayerSettings.h`, `Common/PerfTimer.h`, `Common/Player.h`, `Common/PlayerList.h`, `Common/PlayerTemplate.h`, `Common/Radar.h`, `Common/Recorder.h`, `Common/SpecialPower.h`, `Common/StatsCollector.h`, `Common/ThingTemplate.h`, `Common/GameLOD.h`, `GameClient/InGameUI.h`, `GameClient/CommandXlat.h`, `GameClient/DebugDisplay.h`, `GameClient/Drawable.h`, `GameClient/GameClient.h`, `GameClient/GameWindowManager.h`, `GameClient/GameText.h`, `GameClient/ParticleSys.h`, `GameClient/GUICallbacks.h`, `GameClient/Shell.h`, `GameClient/ControlBar.h`, `GameClient/SelectionInfo.h`, `GameClient/SelectionXlat.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/GameLogic.h`,
