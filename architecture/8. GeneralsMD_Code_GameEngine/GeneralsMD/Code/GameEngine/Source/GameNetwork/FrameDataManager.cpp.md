# GeneralsMD/Code/GameEngine/Source/GameNetwork/FrameDataManager.cpp

## Purpose
Manages frame-based network command data for local or remote players in the game.

## Responsibilities
- Initializes and resets frame data structures
- Adds network commands to specific frames
- Tracks command readiness and counts per frame
- Handles game quit state and frame zeroing

## Key Types
- FrameDataManager (Class): manages frame data for network commands
- FrameData (Class): stores commands for a specific frame
- NetCommandMsg (Class): network command message type
- NetCommandList (Class): list of network commands

## Key Functions
### FrameDataManager::addNetCommandMsg
- Purpose: Adds a network command to the appropriate frame
- Calls: `getExecutionFrame`, `addCommand`, `getCommandCount`, `setFrameCommandCount`

### FrameDataManager::allCommandsReady
- Purpose: Checks if all commands for a given frame are ready
- Calls: `allCommandsReady` (from FrameData)

### FrameDataManager::resetFrame
- Purpose: Resets the contents of a specific frame
- Calls: `reset`, `setFrame`, `setFrameCommandCount`, `getCommandCount`

### FrameDataManager::zeroFrames
- Purpose: Resets command counts for a range of frames
- Calls: `zeroFrame` (from FrameData)

## Globals
- None

## Dependencies
- `FrameDataManager.h`
- `NetworkUtil.h`
- `PreRTS.h`
- `NetCommandMsg`
- `NetCommandList`
- `FrameData`
