# GeneralsMD/Code/GameEngine/Source/GameNetwork/FrameData.cpp

## Purpose
Manages network command data for a specific game frame, tracking command reception and readiness.

## Responsibilities
- Initialize and reset frame data structures
- Track command reception status per frame
- Manage command list (addition, retrieval, cleanup)
- Debug logging for command synchronization issues

## Key Types
- **FrameData (Class)**: Main class handling frame command data
- **FrameDataReturnType (Enum)**: Return status for command readiness checks

## Key Functions
### `allCommandsReady`
- Purpose: Checks if all expected commands for the frame have been received
- Calls: `DEBUG_LOG`

### `addCommand`
- Purpose: Adds a network command to the frame's command list
- Calls: `m_commandList->findMessage`, `m_commandList->addMessage`

### `destroyGameMessages`
- Purpose: Clears all commands from the frame
- Calls: `m_commandList->reset`

## Globals
- **m_frame (UnsignedInt)**: Current frame number
- **m_commandList (NetCommandList**)**: List of commands for this frame
- **m_commandCount (UnsignedInt)**: Number of commands received
- **m_frameCommandCount (UnsignedInt)**: Expected number of commands
- **m_lastFailedCC (UnsignedInt)**: Last failed command count for debugging
- **m_lastFailedFrameCC (UnsignedInt)**: Last failed frame command count

## Dependencies
- `FrameData.h`, `NetworkUtil.h`
- `NetCommandList`, `NetCommandMsg`, `NetCommandRef` classes
- `DEBUG_LOG` macro
- `newInstance` template function
