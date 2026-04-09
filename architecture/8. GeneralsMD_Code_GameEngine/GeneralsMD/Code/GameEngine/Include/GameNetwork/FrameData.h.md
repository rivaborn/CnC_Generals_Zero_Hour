# GeneralsMD/Code/GameEngine/Include/GameNetwork/FrameData.h

## Purpose
Manages frame-based command data for network synchronization in the game.

## Responsibilities
- Tracks frame number and command state
- Manages a list of network commands per frame
- Handles command readiness checks and resends
- Provides frame command count tracking

## Key Types
- FrameDataReturnType (Enum): Command readiness status (not ready, resend, ready)
- FrameData (Class): Main class for frame data management

## Key Functions
### FrameData::update
- Purpose: Updates frame data state.
- Calls: Not inferable.

### FrameData::allCommandsReady
- Purpose: Checks if all commands for current frame are ready.
- Calls: Not inferable.

### FrameData::addCommand
- Purpose: Adds a network command to the current frame.
- Calls: Not inferable.

### FrameData::destroyGameMessages
- Purpose: Cleans up game messages/commands.
- Calls: Not inferable.

## Globals
None

## Dependencies
- `Lib/BaseType.h` (for UnsignedInt, Bool)
- `GameNetwork/NetCommandList.h` (for NetCommandList, NetCommandMsg)
