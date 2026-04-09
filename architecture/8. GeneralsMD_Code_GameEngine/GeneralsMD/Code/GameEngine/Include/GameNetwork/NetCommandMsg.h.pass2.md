# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetCommandMsg.h - Enhanced Analysis

## Architectural Role
This file defines the core network message hierarchy for the SAGE engine's multiplayer system, serving as the abstraction layer between high-level game commands and low-level network transmission. It implements a command pattern for network operations, enabling reliable message delivery with acknowledgment tracking and chunked data transfer.

## Cross-References
### Incoming
- Networking subsystem (e.g., `NetClient`, `NetServer`) - uses these message classes for serialization/deserialization
- Game message system (`GameMessage`) - constructs game-specific messages from network data
- Memory management system - utilizes `MemoryPoolObject` for allocation

### Outgoing
- Calls into `GameMessage` and `GameMessageArgument` for message construction
- Relies on `NetworkDefs.h` for type definitions and constants
- Uses `UnicodeString` for string handling in file transfer messages

## Design Patterns
- **Command Pattern**: Encapsulates network operations as objects, enabling queuing and execution at specific frames
- **Composite Pattern**: `NetCommandMsg` serves as a base class with various derived message types forming a hierarchy
- **Flyweight Pattern**: Memory pooling via `MemoryPoolObject` reduces allocation overhead for frequently created messages
