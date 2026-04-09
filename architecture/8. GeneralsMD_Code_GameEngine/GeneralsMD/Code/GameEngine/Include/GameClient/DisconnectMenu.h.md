# GeneralsMD/Code/GameEngine/Include/GameClient/DisconnectMenu.h

## Purpose
Header for the DisconnectMenu class, managing in-game disconnect/timeout UI and player voting.

## Responsibilities
- Manage disconnect menu visibility and state
- Display player timeout status and voting controls
- Handle chat and player removal actions
- Interface with DisconnectManager for game state updates

## Key Types
- **DisconnectMenuStateType (Enum)**: Menu visibility state (on/off)
- **DisconnectMenu (Class)**: Main menu controller for disconnects and voting

## Key Functions
### DisconnectMenu::init
- Purpose: Initialize menu controls and resources
- Calls: Not inferable

### DisconnectMenu::attachDisconnectManager
- Purpose: Link to DisconnectManager for status updates
- Calls: Not inferable

### DisconnectMenu::showScreen / hideScreen
- Purpose: Toggle menu visibility
- Calls: Not inferable

### DisconnectMenu::voteForPlayer / updateVotes
- Purpose: Handle player voting mechanics
- Calls: Not inferable

### DisconnectMenu::quitGame / removePlayer
- Purpose: Handle game exit and player removal
- Calls: Not inferable

## Globals
- **TheDisconnectMenu (DisconnectMenu*)**: Singleton instance of the disconnect menu

## Dependencies
- "GameNetwork/DisconnectManager.h" (DisconnectManager)
- UnicodeString, Bool, Int, time_t (standard types)
- MAX_SLOTS (constant for player slots)
