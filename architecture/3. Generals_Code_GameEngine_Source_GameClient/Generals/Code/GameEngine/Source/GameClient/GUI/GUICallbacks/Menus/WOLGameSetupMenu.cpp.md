# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLGameSetupMenu.cpp

## Purpose
Handles the Westwood Online (WOL) game setup menu UI and logic for multiplayer staging rooms.

## Responsibilities
- Manages player slot configuration (color, faction, team, start position)
- Handles chat and emotes
- Coordinates game start and lobby navigation
- Displays player stats and tooltips
- Manages map selection and preview

## Key Types
- `WOLGameSetupMenuSystem` (Function): Main window system callback for the game setup menu
- `GameSpyStagingRoom` (External): Represents the multiplayer staging room
- `GameSpyGameSlot` (External): Represents individual player slots
- `PeerRequest` (External): Network request structure

## Key Functions
### `WOLGameSetupMenuSystem`
- Purpose: Main window system callback handling UI events
- Calls: `handleColorSelection`, `handlePlayerTemplateSelection`, `handleTeamSelection`, `StartPressed`, `WOLDisplaySlotList`, `handleStartPositionSelection`, `handleGameSetupSlashCommands`

### `StartPressed`
- Purpose: Initiates game start when host clicks Start button
- Calls: `TheGameSpyInfo->startGame`, `TheShell->pop`

### `handleStartPositionSelection`
- Purpose: Assigns/unassigns start positions to players
- Calls: `TheGameSpyInfo->setGameOptions`, `WOLDisplaySlotList`

### `playerTooltip`
- Purpose: Generates detailed player info tooltips
- Calls: `TheMouse->setCursorTooltip`, `TheGameSpyPSMessageQueue->findPlayerStatsByID`

### `SendStatsToOtherPlayers`
- Purpose: Broadcasts player statistics to other clients
- Calls: `TheGameSpyPeerMessageQueue->addRequest`

## Globals
- `parentWOLGameSetupID` (NameKeyType): ID of parent window
- `comboBoxPlayerID` (NameKeyType[MAX_SLOTS]): IDs for player selection comboboxes
- `buttonAcceptID` (NameKeyType[MAX_SLOTS]): IDs for accept buttons
- `initDone` (Bool): Tracks initialization state
- `WOLMapSelectLayout` (WindowLayout*): Map selection UI layout

## Dependencies
- GameClient headers: `GameWindowManager.h`, `GadgetComboBox.h`, `GadgetListBox.h`
- GameNetwork headers: `GameSpy/PeerDefs.h`, `GameSpy/PeerThread.h`
- Common headers: `MultiplayerSettings.h`, `PlayerTemplate.h`
