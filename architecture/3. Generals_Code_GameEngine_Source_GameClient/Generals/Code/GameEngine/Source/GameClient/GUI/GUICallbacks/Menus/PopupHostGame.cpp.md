# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupHostGame.cpp

## Purpose
Handles the UI callbacks for the "Host Game" popup menu in Command & Conquer Generals.

## Responsibilities
- Manages game creation UI elements (name, password, observers, etc.)
- Populates ladder selection dropdowns
- Handles user input for hosting a game
- Manages ladder preferences and selections
- Initiates game creation via GameSpy network

## Key Types
- `GameWindow` (Type): UI window handle
- `CustomMatchPreferences` (Class): Stores custom match settings
- `LadderInfo` (Struct): Contains ladder connection details
- `PeerRequest` (Struct): GameSpy network request structure

## Key Functions
### `createGame()`
- Purpose: Initiates game creation with current UI settings
- Calls: `TheGameSpyGame->setGameName()`, `TheGameSpyGame->setAllowObservers()`, `TheGameSpyPeerMessageQueue->addRequest()`

### `PopulateCustomLadderComboBox()`
- Purpose: Fills ladder dropdown with available ladders
- Calls: `GadgetComboBoxReset()`, `GadgetComboBoxAddEntry()`, `TheLadderList->findLadder()`

### `PopupHostGameSystem()`
- Purpose: Handles system messages for the host game window
- Calls: `GadgetTextEntryGetText()`, `GadgetComboBoxGetSelectedPos()`, `GameSpyCloseOverlay()`

## Globals
- `parentPopup` (GameWindow*): Main popup window handle
- `textEntryGameName` (GameWindow*): Game name input field
- `comboBoxLadderName` (GameWindow*): Ladder selection dropdown
- `isPopulatingLadderBox` (bool): Flag for ladder population state

## Dependencies
- GameSpy network components (`PeerThread.h`, `GameSpyOverlay.h`)
- UI components (`GadgetComboBox.h`, `GadgetTextEntry.h`)
- Game data (`GlobalData.h`, `CustomMatchPreferences.h`)
- Window management (`WindowLayout.h`)
