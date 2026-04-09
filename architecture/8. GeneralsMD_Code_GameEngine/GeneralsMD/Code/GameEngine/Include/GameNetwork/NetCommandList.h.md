# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetCommandList.h

## Purpose
Defines a linked list structure for managing ordered `NetCommandRef` objects used in network command processing.

## Responsibilities
- Maintains an ordered list of network commands by command ID, player ID, and type
- Provides methods to add, find, remove, and traverse commands
- Optimizes for sequential insertion of commands
- Supports list merging and length calculation

## Key Types
- **NetCommandList (Class)**: Manages an ordered list of network commands
- **NetCommandListMagicEnum (Enum)**: Not inferable (likely internal memory pool tag)
- **NetCommandList_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal memory pool tag)

## Key Functions
### `addMessage`
- Purpose: Adds a network command message to its proper ordered position in the list
- Calls: Not inferable (implementation in .cpp)

### `findMessage`
- Purpose: Locates a command message by reference or by command ID/player ID
- Calls: Not inferable

### `removeMessage`
- Purpose: Removes a specified command reference from the list
- Calls: Not inferable

### `appendList`
- Purpose: Merges another command list onto the end of this one
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/GameMemory.h` (for `MemoryPoolObject`)
- `GameNetwork/NetCommandRef.h` (for `NetCommandRef` and `NetCommandMsg`)
- Uses `Bool`, `UnsignedShort`, `UnsignedByte`, `Int` (likely from common types)
