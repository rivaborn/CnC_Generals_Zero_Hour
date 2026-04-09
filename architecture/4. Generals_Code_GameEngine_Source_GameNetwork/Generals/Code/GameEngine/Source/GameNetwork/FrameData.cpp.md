# Generals/Code/GameEngine/Source/GameNetwork/FrameData.cpp

## Purpose
Manages frame-based command data for network synchronization in the game engine.

## Responsibilities
- Tracks command execution state per game frame
- Manages a list of network commands (NetCommandList)
- Handles command synchronization and validation
- Provides frame command count tracking

## Key Types
- **FrameData (Class)**: Main class handling frame command data
- **NetCommandList (Class)**: Command list container (external)
- **NetCommandMsg (Class)**: Network command message (external)

## Key Functions
### `allCommandsReady`
- Purpose: Checks if all expected commands for a frame have been received
- Calls: `DEBUG_LOG`, `m_commandList->getFirstMessage`, `ref->getNext`

### `addCommand`
- Purpose: Adds a network command to the current frame
- Calls: `init`, `m_commandList->findMessage`, `m_commandList->addMessage`

### `destroyGameMessages`
- Purpose: Clears all commands from the current frame
- Calls: `m_commandList->reset`

## Globals
- **m_frame (UnsignedInt)**: Current frame number
- **m_commandList (NetCommandList**)**: List of commands for this frame
- **m_commandCount (UnsignedInt)**: Number of commands received
- **m_frameCommandCount (UnsignedInt)**: Expected command count for this frame

## Dependencies
- `FrameData.h`, `NetworkUtil.h`
- `NetCommandList`, `NetCommandMsg` (external)
- `DEBUG_LOG` macro
- `newInstance` template function
