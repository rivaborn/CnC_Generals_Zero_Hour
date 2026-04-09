# Generals/Code/GameEngine/Source/GameNetwork/NetCommandList.cpp

## Purpose
Manages a sorted list of network command messages for the game's networking system.

## Responsibilities
- Maintains a doubly-linked list of `NetCommandRef` objects
- Provides insertion, removal, and search operations for network commands
- Ensures commands are sorted by type, player ID, and command ID
- Handles command deduplication to prevent duplicates in the list
- Supports appending entire command lists

## Key Types
- `NetCommandList` (Class): Manages the sorted list of network commands
- `NetCommandRef` (Class): Reference-counted wrapper for network command messages
- `NetCommandMsg` (Class): Base class for network command messages

## Key Functions
### `addMessage`
- Purpose: Inserts a new command message into the sorted list
- Calls: `NEW_NETCOMMANDREF`, `isEqualCommandMsg`, `DoesCommandRequireACommandID`

### `removeMessage`
- Purpose: Removes a specific message from the list
- Calls: None (directly manipulates list pointers)

### `findMessage`
- Purpose: Searches for a message matching specific criteria
- Calls: `isEqualCommandMsg`, `DoesCommandRequireACommandID`

### `isEqualCommandMsg`
- Purpose: Determines if two command messages are equivalent
- Calls: `DoesCommandRequireACommandID`

## Globals
- None

## Dependencies
- `NetCommandList.h` (header for this class)
- `NetworkUtil.h` (for utility functions like `DoesCommandRequireACommandID`)
- `PreRTS.h` (engine precompiled header)
- Various network command message types (e.g., `NetAckStage1CommandMsg`)
