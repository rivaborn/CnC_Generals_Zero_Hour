# GeneralsMD/Code/GameEngine/Source/GameLogic/ScriptEngine/VictoryConditions.cpp

## Purpose
Manages multiplayer victory and defeat conditions in Command & Conquer Generals Zero Hour.

## Responsibilities
- Tracks player elimination based on victory conditions (no units/buildings)
- Determines when a single alliance remains as winner
- Handles local player defeat detection
- Caches player pointers for reference
- Provides interface for victory/defeat state queries

## Key Types
- **VictoryConditions (Class)**: Core class implementing victory condition logic
- **VictoryConditionsInterface (Class)**: Interface for victory condition system (defined elsewhere)

## Key Functions
### areAllies
- Purpose: Checks if two players are allies
- Calls: Player::getRelationship

### createVictoryConditions
- Purpose: Factory function to create VictoryConditions instance
- Calls: None

### VictoryConditions::update
- Purpose: Updates victory/defeat state each frame
- Calls: TheRecorder->isMultiplayer, hasSinglePlayerBeenDefeated, ThePartitionManager->revealMapForPlayerPermanently, TheGameClient->updateFakeDrawables, TheInGameUI->message, TheAudio->addAudioEvent, Player::killPlayer, PopulateInGameDiplomacyPopup, TheRadar->forceOn, SetInGameChatType

### VictoryConditions::hasSinglePlayerBeenDefeated
- Purpose: Determines if a player has been defeated based on victory conditions
- Calls: Player::hasAnyObjects, Player::hasAnyUnits, Player::hasAnyBuildings

### VictoryConditions::cachePlayerPtrs
- Purpose: Caches pointers to active players at game start
- Calls: TheRecorder->isMultiplayer, ThePlayerTemplateStore->findPlayerTemplate, ThePlayerList->getNthPlayer, ThePlayerList->getNeutralPlayer, Player::isLocalPlayer, Player::isPlayerObserver

## Globals
- **TheVictoryConditions (VictoryConditionsInterface*)**: Global pointer to victory conditions instance

## Dependencies
- Common/AudioEventRTS.h, Common/GameAudio.h, Common/GameCommon.h, Common/GameEngine.h, Common/KindOf.h, Common/PlayerList.h, Common/Player.h, Common/PlayerTemplate.h, Common/Radar.h, Common/Recorder.h
- GameClient/InGameUI.h, GameClient/Diplomacy.h, GameClient/GameText.h, GameClient/GUICallbacks.h, GameClient/MessageBox.h, GameClient/GameClient.h
- GameLogic/GameLogic.h, GameLogic/PartitionManager.h, GameLogic/ScriptActions.h, GameLogic/VictoryConditions.h
- GameNetwork/GameInfo.h, GameNetwork/NetworkDefs.h
