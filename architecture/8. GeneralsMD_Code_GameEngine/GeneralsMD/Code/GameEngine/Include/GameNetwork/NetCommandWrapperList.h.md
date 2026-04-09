# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetCommandWrapperList.h

## Purpose
Manages a list of network command wrappers for fragmented or delayed network messages.

## Responsibilities
- Tracks fragmented network commands via `NetCommandWrapperListNode`
- Processes incoming command chunks and reassembles complete commands
- Provides ready commands to the game network system
- Tracks completion percentage of wrapped commands

## Key Types
- **NetCommandWrapperListNode (Class)**: Represents a single fragmented network command and its reassembly state.
- **NetCommandWrapperListNodeMagicEnum (Enum)**: Not inferable (likely glue code enum).
- **NetCommandWrapperListNode_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely glue code enum).
- **NetCommandWrapperList (Class)**: Manages the collection of fragmented commands and their reassembly.
- **NetCommandWrapperListMagicEnum (Enum)**: Not inferable (likely glue code enum).
- **NetCommandWrapperList_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely glue code enum).

## Key Functions
### NetCommandWrapperListNode::isComplete
- Purpose: Checks if all chunks of a fragmented command have been received.
- Calls: Not inferable.

### NetCommandWrapperList::processWrapper
- Purpose: Processes an incoming network command chunk and updates the reassembly state.
- Calls: Not inferable.

### NetCommandWrapperList::getReadyCommands
- Purpose: Retrieves a list of fully reassembled commands ready for execution.
- Calls: Not inferable.

### NetCommandWrapperList::getPercentComplete
- Purpose: Returns the reassembly progress percentage for a specific wrapped command.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `GameNetwork/NetCommandList.h`
- `MemoryPoolObject` (base class)
- `NetWrapperCommand
