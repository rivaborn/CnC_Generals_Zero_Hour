# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/LobbyUtils.h

## Purpose
Header file providing utility functions for the Generals lobby UI, including game list management and sorting.

## Responsibilities
- Declares functions for managing lobby UI elements (list boxes, tooltips).
- Defines sorting types for game lists.
- Provides accessors for lobby window components.

## Key Types
- GameWindow (Class): UI window handle.
- GameSortType (Enum): Sorting criteria for game lists (alpha/ascending/descending, ping).

## Key Functions
### GetGameListBox
- Purpose: Retrieves the game list box window.
- Calls: None.

### GetGameInfoListBox
- Purpose: Retrieves the game info list box window.
- Calls: None.

### HandleSortButton
- Purpose: Handles sorting button clicks.
- Calls: None.

### PopulateLobbyPlayerListbox
- Purpose: Populates the player list box in the lobby.
- Calls: None.

## Globals
None.

## Dependencies
- `GameWindow` (external class).
- `NameKeyType`, `WinInstanceData`, `UnsignedInt`, `Bool` (external types).
