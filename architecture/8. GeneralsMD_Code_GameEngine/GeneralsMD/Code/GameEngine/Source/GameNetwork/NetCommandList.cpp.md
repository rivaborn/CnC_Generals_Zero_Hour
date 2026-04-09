# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetCommandList.cpp

## Purpose
Manages a sorted list of network command messages for the game's networking system.

## Responsibilities
- Maintains a doubly-linked list of `NetCommandRef` objects
- Provides insertion, removal, and lookup operations
- Ensures commands are sorted by type, player ID, and command ID
- Handles command deduplication

## Key Types
- `NetCommandList` (Class): Manages the list of network commands
- `NetCommandRef` (Class): Reference-counted wrapper for network commands
- `NetCommandMsg` (Class): Base class for network command messages

## Key Functions
### `addMessage`
- Purpose: Inserts a command message into the sorted list
- Calls: `NEW_NETCOMMANDREF`, `isEqualCommandMsg`

### `removeMessage`
- Purpose: Removes a specific message from the list
- Calls: None

### `findMessage`
- Purpose: Locates a message by command ID and player ID
- Calls: `DoesCommandRequireACommandID`

### `isEqualCommandMsg`
- Purpose: Compares two command messages for equality
- Calls: `DoesCommandRequireACommandID`

## Globals
- None

## Dependencies
- `NetCommandList.h`
- `NetworkUtil.h`
- `PreRTS.h`
- `NEW_NETCOMMANDREF` macro
- `DoesCommandRequireACommandID` function
- Various `NetCommandMsg` subclasses (e.g., `NetAckStage1CommandMsg`)
