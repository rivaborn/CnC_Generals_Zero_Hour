# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/PlaceEventTranslator.cpp

## Purpose
Handles translation of raw input messages into game actions for placing buildings or structures.

## Responsibilities
- Processes mouse input (clicks, drags) during building placement
- Validates placement legality using BuildAssistant
- Generates game messages for construction (MSG_DOZER_CONSTRUCT, MSG_DOZER_CONSTRUCT_LINE)
- Manages placement UI state (anchors, cursors)
- Handles special power construction cases

## Key Types
- **PlaceEventTranslator (Class)**: Main translator class for placement events
- **GameMessageDisposition (Enum)**: Message processing result (KEEP_MESSAGE/DESTROY_MESSAGE)

## Key Functions
### `translateGameMessage`
- Purpose: Routes and processes game messages related to building placement
- Calls: `TheInGameUI->getPendingPlaceType()`, `TheBuildAssistant->isLocationLegalToBuild()`, `TheMessageStream->appendMessage()`

### `pickAndPlayUnitVoiceResponse`
- Purpose: Plays appropriate voice response for construction actions
- Calls: Not visible in this file (external)

## Globals
- **m_frameOfUpButton (Int)**: Tracks frame when placement was confirmed

## Dependencies
- Key includes: `PreRTS.h`, `Common/BuildAssistant.h`, `GameClient/PlaceEventTranslator.h`
- External symbols: `TheInGameUI`, `TheBuildAssistant`, `TheMessageStream`, `TheGameLogic`, `TheAudio`, `TheEva`, `TheTacticalView`, `ThePlayerList`
