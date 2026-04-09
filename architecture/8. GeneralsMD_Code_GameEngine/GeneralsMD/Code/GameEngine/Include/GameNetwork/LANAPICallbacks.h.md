# GeneralsMD/Code/GameEngine/Include/GameNetwork/LANAPICallbacks.h

## Purpose
Header file defining LAN API callbacks and related types for the game's networking UI.

## Responsibilities
- Declares LAN API singleton and UI gadget references
- Defines color constants for chat dialogs
- Declares callback functions for LAN game management
- Provides enum for LAN game option posting types

## Key Types
- **PostToLanGameType (Enum)**: Type for LAN game option posting operations
- **SEND_GAME_OPTS (Enum value)**: Post game options
- **MAP_BACK (Enum value)**: Post map selection
- **POST_TO_LAN_GAME_TYPE_COUNT (Enum value)**: Count of post types

## Key Functions
### lanUpdateSlotList
- Purpose: Update the slot list in LAN UI
- Calls: Not inferable

### updateGameOptions
- Purpose: Update game options in LAN UI
- Calls: Not inferable

### PostToLanGameOptions
- Purpose: Utility function for posting LAN game options
- Calls: Not inferable

## Globals
- **TheLAN (LANAPI*)**: LAN API singleton instance
- **listboxChatWindowID (NameKeyType)**: ID for chat window listbox
- **listboxChatWindow (GameWindow*)**: Chat window gadget
- **listboxPlayers (GameWindow*)**: Players list gadget
- **listboxGamesID (NameKeyType)**: ID for games listbox
- **listboxGames (GameWindow*)**: Games list gadget
- **listboxChatWindowLanGameID (NameKeyType)**: ID for LAN game options listbox
- **listboxChatWindowLanGame (GameWindow*)**: LAN game options gadget
- **mapSelectLayout (WindowLayout*)**: Map selection layout
- **listboxChatWindow
