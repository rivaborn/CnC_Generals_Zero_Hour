# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanGameOptionsMenu.cpp

## Purpose
Handles the LAN game options menu UI, including player slots, map selection, and game start logic.

## Responsibilities
- Manages player slot configuration (state, color, template, team, start position)
- Handles game start validation and acceptance
- Controls map selection and start position assignment
- Manages chat and emote functionality
- Updates UI based on LAN game state changes

## Key Types
- `LANGameInfo`: LAN game state and slot management
- `GameWindow`: UI window base class
- `WindowLayout`: UI layout management
- `PostToLanGameType`: Enum for menu post messages

## Key Functions
### `StartPressed`
- Purpose: Validates and initiates game start
- Calls: `TheLAN->RequestGameStart`, `TheLAN->RequestGameStartTimer`, `LANEnableStartButton`

### `handleColorSelection`
- Purpose: Updates player color selection
- Calls: `TheLAN->RequestGameOptions`

### `handleStartPositionSelection`
- Purpose: Assigns/unassigns start positions to players
- Calls: `TheLAN->RequestGameOptions`

### `LanGameOptionsMenuSystem`
- Purpose: Handles UI system messages (selection, input)
- Calls: `handleColorSelection`, `handlePlayerTemplateSelection`, `handleTeamSelection`, `StartPressed`

### `PostToLanGameOptions`
- Purpose: Bridges external messages to this menu
- Calls: `updateGameOptions`, `lanUpdateSlotList`, `TheLAN->RequestGameOptions`

## Globals
- `LANnextScreen` (char*): Next screen to transition to
- `LANisShuttingDown` (Bool): Shutdown flag
- `LANbuttonPushed` (Bool): Button press state
- `parentLanGameOptionsID` (NameKeyType): Parent window ID
- `comboBoxPlayerID` (NameKeyType[MAX_SLOTS]): Player slot combo box IDs
- `buttonAcceptID` (NameKeyType[MAX_SLOTS]): Accept button IDs
- `parentLanGameOptions` (GameWindow*): Parent window pointer

## Dependencies
- `GameNetwork/LANAPI.h`, `GameNetwork/LANAPICallbacks.h`
- `GameClient/GadgetComboBox.h`, `GameClient/GadgetPushButton.h`
- `Common/MultiplayerSettings.h`, `GameClient/GameText.h`
- `GameNetwork/GUIUtil.h`
