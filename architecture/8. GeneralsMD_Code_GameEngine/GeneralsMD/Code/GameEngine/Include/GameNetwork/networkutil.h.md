# GeneralsMD/Code/GameEngine/Include/GameNetwork/networkutil.h

## Purpose
Provides utility functions for network operations in the game engine.

## Responsibilities
- IP address resolution
- Command ID generation and management
- Command type checking and conversion
- Debug logging for network buffers

## Key Types
None

## Key Functions
### ResolveIP
- Purpose: Resolves a hostname to an IP address.
- Calls: Not inferable

### GenerateNextCommandID
- Purpose: Generates the next available command ID.
- Calls: Not inferable

### DoesCommandRequireACommandID
- Purpose: Checks if a command type requires a command ID.
- Calls: Not inferable

### CommandRequiresAck
- Purpose: Determines if a command message requires acknowledgment.
- Calls: Not inferable

### CommandRequiresDirectSend
- Purpose: Checks if a command message requires direct sending.
- Calls: Not inferable

### IsCommandSynchronized
- Purpose: Checks if a command type is synchronized.
- Calls: Not inferable

### GetAsciiNetCommandType
- Purpose: Converts a network command type to its ASCII string representation.
- Calls: Not inferable

## Globals
### LOGBUFFER (Macro)
- Purpose: Conditionally logs network buffer contents for debugging.

## Dependencies
- `GameNetwork/NetworkDefs.h`
- `GameNetwork/NetworkInterface.h`
- `AsciiString`, `UnsignedInt`, `UnsignedShort`, `Bool`, `NetCommandType`, `NetCommandMsg` (from included headers)
