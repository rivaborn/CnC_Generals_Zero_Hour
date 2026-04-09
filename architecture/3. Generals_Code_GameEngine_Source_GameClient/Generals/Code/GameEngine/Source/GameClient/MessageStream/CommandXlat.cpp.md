# Generals/Code/GameEngine/Source/GameClient/MessageStream/CommandXlat.cpp

## Purpose
Handles translation of raw input events into tactical commands and processes game messages.

## Responsibilities
- Translates game messages into actions
- Manages unit voice responses
- Handles debug/demo commands
- Validates attack/salvage capabilities
- Locates command centers

## Key Types
- (anonymous enum) (Enum): Not inferable.
- DROPPED_MAX_PARTICLE_COUNT (Enum): Maximum particle count threshold.
- CommandCenterLocator (Class): Locates command centers or expensive buildings.
- HeroHolder (Class): Manages hero units.

## Key Functions
### isSystemMessage
- Purpose: Checks if a message is a system message.
- Calls: None.

### canSelectionSalvage
- Purpose: Determines if selected units can salvage a target.
- Calls: TheInGameUI->getAllSelectedDrawables().

### canObjectForceAttack
- Purpose: Checks if an object can force attack a target or position.
- Calls: obj->isAbleToAttack(), obj->getAbleToAttackSpecificObject(), obj->getAbleToUseWeaponAgainstTarget().

### canAnyForceAttack
- Purpose: Checks if any selected object can force attack a target or position.
- Calls: canObjectForceAttack.

### pickAndPlayUnitVoiceResponse
- Purpose: Plays voice responses for selected units based on message type.
- Calls: templ->getPerUnitSound(), templ->getVoiceSelect(), templ->getVoiceMove().

### findCommandCenterOrMostExpensiveBuilding
- Purpose: Finds the command center or the most expensive building.
- Calls: None.

### viewCommandCenter
- Purpose: Views the command center.
- Calls: None.

### amIAHero
- Purpose: Checks if the player is a hero.
- Calls: None.

### iNeedAHero
- Purpose: Checks if the player needs a hero.
- Calls: None.

## Globals
- TheSkateDistOverride (Real): Override for skate distance (debug).
- DROPPED_MAX_PARTICLE_COUNT (Enum): Maximum particle count threshold.

## Dependencies
- Common/AudioAffect.h, Common/ActionManager.h, Common/GameAudio.h, Common/GameEngine.h, Common/GameType.h, Common/GlobalData.h, Common/MessageStream.h, Common/MiscAudio.h, Common/MultiplayerSettings.h, Common/PerfTimer.h, Common/Player.h, Common/PlayerList.h, Common/PlayerTemplate.h, Common/Radar.h, Common/Recorder.h, Common/SpecialPower.h, Common/StatsCollector.h, Common/ThingTemplate.h, Common/GameLOD.h, GameClient/InGameUI.h, GameClient/CommandXlat.h, GameClient/DebugDisplay.h, GameClient/Drawable.h, GameClient/GameClient.h, GameClient/GameWindowManager.h, GameClient/GameText.h, GameClient/ParticleSys.h, GameClient/GUICallbacks.h, GameClient/Shell.h, GameClient/ControlBar.h, GameClient/SelectionInfo.h, GameClient/SelectionXlat.h, GameLogic/Module/AIUpdate.h, GameLogic/ExperienceTracker.h, GameLogic/GameLogic.h, GameLogic/Module/BodyModule.h, GameLogic/Object.h, GameLogic/PartitionManager.h, GameLogic/ScriptEngine.h, GameLogic/TerrainLogic.h, GameLogic/GhostObject.h, GameLogic/Weapon.h, GameLogic/Module/SpawnBehavior.h, GameLogic/Module/SpecialPowerModule.h, Common/ThingFactory.h, GameLogic/Module/ContainModule.h, GameNetwork/NetworkInterface.h, GameNetwork/GameInfo.h, Game
