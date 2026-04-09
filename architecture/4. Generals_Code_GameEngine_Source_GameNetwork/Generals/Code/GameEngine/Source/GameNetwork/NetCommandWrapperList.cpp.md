# Generals/Code/GameEngine/Source/GameNetwork/NetCommandWrapperList.cpp

## Purpose
Manages a list of network command wrappers, tracking chunked command data and reconstructing complete commands.

## Responsibilities
- Maintains a linked list of `NetCommandWrapperListNode` objects
- Tracks progress of chunked command data reception
- Reconstructs complete commands from received chunks
- Removes completed commands from the list

## Key Types
- **NetCommandWrapperListNode (Class)**: Represents a single command being reconstructed from chunks
- **NetCommandWrapperList (Class)**: Manages the collection of command wrappers

## Key Functions
### NetCommandWrapperListNode::copyChunkData
- Purpose: Copies chunk data into the node's buffer
- Calls: `memcpy`

### NetCommandWrapperList::processWrapper
- Purpose: Processes an incoming wrapper command message
- Calls: `newInstance`, `NetCommandWrapperListNode` constructor

### NetCommandWrapperList::getReadyCommands
- Purpose: Retrieves all complete commands from the list
- Calls: `newInstance`, `NetPacket::ConstructNetCommandMsgFromRawData`, `NetCommandList::addMessage`

### NetCommandWrapperList::removeFromList
- Purpose: Removes a node from the linked list
- Calls: `deleteInstance`

## Globals
- None

## Dependencies
- `NetCommandWrapperList.h`
- `NetPacket.h`
- `PreRTS.h`
- `NetWrapperCommandMsg`
- `NetCommandRef`
- `NetCommandList`
