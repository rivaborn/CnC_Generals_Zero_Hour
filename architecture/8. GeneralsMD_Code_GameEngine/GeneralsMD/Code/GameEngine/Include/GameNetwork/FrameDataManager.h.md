# GeneralsMD/Code/GameEngine/Include/GameNetwork/FrameDataManager.h

## Purpose
Manages frame-based network command data for synchronization in multiplayer.

## Responsibilities
- Tracks network commands per frame
- Manages frame advancement and command readiness
- Handles local vs. remote command differentiation
- Provides frame data access and manipulation

## Key Types
- **FrameDataManager (Class)**: Manages frame data and network commands
- **FrameDataManagerMagicEnum (Enum)**: Not inferable
- **FrameDataManager_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### FrameDataManager
- Purpose: Constructor for FrameDataManager
- Calls: Not inferable

### init
- Purpose: Initializes the frame data manager
- Calls: Not inferable

### update
- Purpose: Updates frame data manager state
- Calls: Not inferable

### addNetCommandMsg
- Purpose: Adds a network command message to the manager
- Calls: Not inferable

### allCommandsReady
- Purpose: Checks if all commands for a frame are ready
- Calls: Not inferable

### getFrameCommandList
- Purpose: Retrieves the command list for a specific frame
- Calls: Not inferable

### setQuitFrame/getQuitFrame/getIsQuitting
- Purpose: Manages game quit state and frame
- Calls: Not inferable

## Globals
- **m_frameData (FrameData*)**: Pointer to frame data storage
- **m_isLocal (Bool)**: Flag indicating if this is a local player
- **m_isQuitting (Bool)**: Flag indicating if game is quitting
- **m_quitFrame (UnsignedInt)**: Frame number when quit was initiated

## Dependencies
- `GameNetwork/NetworkDefs.h`
- `GameNetwork/FrameData.h`
