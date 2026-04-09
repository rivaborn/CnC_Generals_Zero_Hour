# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLGameSetupMenu.cpp

## Purpose
Handles the Westwood Online (WOL) game setup menu UI and logic for multiplayer staging rooms.

## Responsibilities
- Manages player slot configuration (color, faction, team, start position)
- Handles game options (map selection, superweapons, starting cash)
- Processes player chat and slash commands
- Synchronizes game state with other players via GameSpy network
- Manages UI tooltips and visual feedback

## Key Types
- `WOLGameSetupMenuSystem`: Main window system callback for the game setup menu
- `GameSpyStagingRoom`: Represents the multiplayer staging room state
- `GameSpyGameSlot`: Represents individual player slots in the staging room
- `CustomMatchPreferences`: Stores player preferences for color/faction/map
- `PeerRequest`: Network message structure for GameSpy communication

## Key Functions
### `SendStatsToOtherPlayers`
- Purpose: Broadcasts player statistics to other players in the staging room
- Calls: `TheGameSpyPeerMessageQueue->addRequest`

### `WOLPositionStartSpots`
- Purpose: Positions start spot buttons on the map preview
- Calls: `positionStartSpots`, `GadgetListBoxGetSelected`

### `StartPressed`
- Purpose: Handles the "Start Game" button press logic
- Calls: `TheGameSpyInfo->startGame`, `WOLDisplaySlotList`

### `handleGameSetupSlashCommands`
- Purpose: Processes slash commands entered in chat
- Calls: `TheGameSpyInfo->sendChat`

### `WOLGameSetupMenuUpdate`
- Purpose: Updates the UI based on current game state
- Calls: `WOLDisplaySlotList`, `WOLDisplayGameOptions`

## Globals
- `TheLobbyQueuedUTMs` (std::list<PeerResponse>): Queued network messages
- `isShuttingDown` (Bool): Tracks if menu is shutting down
- `buttonPushed` (Bool): Tracks button press state
- `parentWOLGameSetup` (GameWindow*): Pointer to parent window
- `comboBoxPlayer` (GameWindow*[MAX_SLOTS]): Player selection combo boxes
- `pingImages` (const Image*[3]): Ping status images

## Dependencies
- GameSpy network components (`PeerThread`, `PersistentStorageThread`)
- UI components (`GadgetComboBox`, `GadgetListBox`, `GadgetTextEntry`)
- Game state management (`GameState`, `MultiplayerSettings`)
- Window management (`WindowLayout`, `GameWindowManager`)
