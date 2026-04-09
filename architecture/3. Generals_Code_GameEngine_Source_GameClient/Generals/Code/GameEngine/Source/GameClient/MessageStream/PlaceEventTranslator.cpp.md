# Generals/Code/GameEngine/Source/GameClient/MessageStream/PlaceEventTranslator.cpp

## Purpose
Handles translation of raw input messages into building placement commands in the game.

## Responsibilities
- Processes mouse input for building placement
- Validates placement legality using BuildAssistant
- Generates and sends placement messages to the game logic
- Manages placement UI state (anchors, cursors)

## Key Types
- PlaceEventTranslator (Class): Translates input messages for building placement
- GameMessageDisposition (Enum): Message processing result (KEEP_MESSAGE, DESTROY_MESSAGE)

## Key Functions
### translateGameMessage
- Purpose: Processes game messages related to building placement
- Calls: TheInGameUI->getPendingPlaceType, TheTacticalView->screenToTerrain, TheBuildAssistant->isLocationLegalToBuild, TheMessageStream->appendMessage, TheInGameUI->placeBuildAvailable, TheInGameUI->displayCantBuildMessage, TheAudio->addAudioEvent

## Globals
- None

## Dependencies
- Common/GameAudio.h, Common/Player.h, Common/PlayerList.h, Common/ThingTemplate.h, Common/BuildAssistant.h
- GameLogic/Object.h, GameLogic/GameLogic.h
- GameClient/CommandXlat.h, GameClient/PlaceEventTranslator.h, GameClient/Drawable.h, GameClient/Eva.h
