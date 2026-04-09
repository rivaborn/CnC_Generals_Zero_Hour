# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarCommandProcessing.cpp

## Purpose
Handles UI command processing for the control bar in Command & Conquer Generals, translating button clicks into game actions.

## Responsibilities
- Processes button transition and selection messages from the UI
- Validates command preconditions (e.g., money, queue space)
- Dispatches game messages for unit production, upgrades, special abilities, etc.
- Manages context-sensitive UI states (e.g., multi-select, observer modes)
- Plays unit-specific audio feedback for commands

## Key Types
- `ControlBar` (Class): Main control bar manager handling command processing
- `CommandButton` (Class): Represents a clickable command button with associated data
- `CBCommandStatus` (Enum): Status codes for command processing results

## Key Functions
### `processCommandTransitionUI`
- Purpose: Handles button transition messages (e.g., hover states)
- Calls: `switchToContext`

### `processCommandUI`
- Purpose: Processes button click commands and dispatches game actions
- Calls: `GadgetButtonGetData`, `TheBuildAssistant->canMakeUnit`, `TheMessageStream->appendMessage`, `TheInGameUI->placeBuildAvailable`, `TheUpgradeCenter->canAffordUpgrade`, `pickAndPlayUnitVoiceResponse`

## Globals
- `TheControlBar` (ControlBar*): Global control bar instance
- `TheInGameUI` (InGameUI*): Global in-game UI manager
- `ThePlayerList` (PlayerList*): Global player list
- `TheMessageStream` (MessageStream*): Global message stream
- `TheEva` (Eva*): Global EVA (EVA) system
- `TheGameLogic` (GameLogic*): Global game logic system
- `TheUpgradeCenter` (UpgradeCenter*): Global upgrade center
- `TheScienceStore` (ScienceStore*): Global science store
- `TheAudio` (Audio*): Global audio system

## Dependencies
- Common: `BuildAssistant`, `Money`, `Player`, `PlayerList`, `Science`, `SpecialPower`, `ThingTemplate`, `Upgrade`, `PlayerTemplate`
- GameClient: `CommandXlat`, `ControlBar`, `Drawable`, `Eva`, `GameClient`, `GadgetPushButton`, `GameWindow`, `GameWindowManager`, `InGameUI`, `AnimateWindowManager`
- GameLogic: `GameLogic`, `Object`, `Module/ProductionUpdate`
