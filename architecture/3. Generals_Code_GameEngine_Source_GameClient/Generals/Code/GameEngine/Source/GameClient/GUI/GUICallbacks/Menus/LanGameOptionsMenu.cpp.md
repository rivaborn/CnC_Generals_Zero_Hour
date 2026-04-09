# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanGameOptionsMenu.cpp

## Purpose
Handles the LAN game options menu UI, including player slots, map selection, and game start logic.

## Responsibilities
- Manages player slot configuration (color, template, team, start position)
- Handles game start validation and acceptance
- Updates UI based on LAN game state changes
- Manages map selection and start position assignment
- Processes chat and emote inputs

## Key Types
- `LANGameInfo` (Class): Represents the current LAN game session
- `LANGameSlot` (Class): Represents a player slot in the LAN game
- `SlotState` (Enum): Defines player slot states (open, closed, player, AI)
- `PostToLanGameType` (Enum): Defines message types for inter-window communication

## Key Functions
### `StartPressed`
- Purpose: Validates game start conditions and initiates game start
- Calls: `TheLAN->RequestGameStart()`, `TheLAN->RequestGameStartTimer()`, `LANEnableStartButton()`

### `handleColorSelection`
- Purpose: Updates player color selection for a slot
- Calls: `GadgetComboBoxGetSelectedPos()`, `TheLAN->RequestGameOptions()`

### `handleStartPositionSelection`
- Purpose: Assigns or removes a player from a map start position
- Calls: `TheLAN->RequestGameOptions()`, `lanUpdateSlotList()`

### `LanGameOptionsMenuSystem`
- Purpose: Handles all UI system messages for the LAN game options menu
- Calls: `handleColorSelection()`, `handlePlayerTemplateSelection()`, `handleTeamSelection()`, `StartPressed()`

### `PostToLanGameOptions`
- Purpose: Bridges messages from other windows to this menu
- Calls: `LanPositionStartSpots()`, `updateGameOptions()`, `lanUpdateSlotList()`

## Globals
- `LANnextScreen` (char*): Stores the next screen to display after shutdown
- `LANisShuttingDown` (Bool): Flag indicating if the menu is shutting down
- `LANbuttonPushed` (Bool): Flag to prevent multiple button presses
- `parentLanGameOptionsID` (NameKeyType): ID for the parent window
- `comboBoxPlayerID` (NameKeyType[MAX_SLOTS]): IDs for player slot combo boxes
- `buttonAcceptID` (NameKeyType[MAX_SLOTS]): IDs for accept buttons per slot
- `parentLanGameOptions` (GameWindow*): Pointer to the parent window

## Dependencies
- `GameNetwork/LANAPI.h`, `GameNetwork/LANAPICallbacks.h`
- `GameClient/GadgetComboBox.h`, `GameClient/GadgetPushButton.h`
- `Common/MultiplayerSettings.h`, `Common/GameEngine.h`
- `GameClient/WindowLayout.h`, `GameClient/Shell.h`
