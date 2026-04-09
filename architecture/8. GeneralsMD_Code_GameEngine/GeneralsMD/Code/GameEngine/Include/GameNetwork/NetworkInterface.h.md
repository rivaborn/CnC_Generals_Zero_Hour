# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetworkInterface.h

## Purpose
Defines the abstract interface for the game's networking subsystem, including packet handling, chat, file transfers, and performance metrics.

## Responsibilities
- Declares pure virtual methods for network operations (init, update, send/receive).
- Defines global functions for command packet management.
- Provides bandwidth and connection status metrics.
- Handles player disconnections and voting.
- Manages file transfers and load progress.

## Key Types
- **NetworkInterface (Class)**: Abstract base class for network operations.
- **CommandPacket (Class)**: Represents network command packets.
- **GameMessage (Class)**: Represents game messages.
- **GameInfo (Class)**: Contains game session information.

## Key Functions
### ClearCommandPacket
- Purpose: Clears the command packet at the start of a frame.
- Calls: None.

### GetCommandPacket
- Purpose: Retrieves the command packet for sending.
- Calls: None.

### ResolveIP
- Purpose: Converts a host string to a 32-bit IP address.
- Calls: None.

## Globals
- **None**

## Dependencies
- `MessageStream.h`, `ConnectionManager.h`, `User.h`, `NetworkDefs.h`
- `SubsystemInterface` (inherited)
- `Transport` (forward-declared)
