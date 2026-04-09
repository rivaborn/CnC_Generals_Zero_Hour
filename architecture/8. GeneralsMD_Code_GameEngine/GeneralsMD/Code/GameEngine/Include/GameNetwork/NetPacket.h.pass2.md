# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetPacket.h - Enhanced Analysis

## Architectural Role
This file defines the core network packet handling class (`NetPacket`) that bridges the game's command system (`NetCommandRef`) with the transport layer (`TransportMessage`). It implements serialization/deserialization for all network message types, acting as the central mediator for network communication in the SAGE engine.

## Cross-References
### Incoming
- `GameNetwork/NetCommandList.h` - Uses `NetCommandList` for command storage
- `Common/MessageStream.h` - Likely used for binary serialization
- `GameEngine/GameLogic/GameMessage.h` - For game-specific message handling

### Outgoing
- Calls into `TransportMessage` for actual network transmission
- Uses `MemoryPoolObject` for memory management
- Interfaces with `NetCommandRef` and `NetCommandMsg` for command processing

## Design Patterns
- **Strategy Pattern**: Each command type has dedicated serialization/deserialization methods (e.g., `FillBufferWithGameCommand`, `readGameMessage`), allowing different handling logic per command type.
- **Factory Pattern**: `ConstructNetCommandMsgFromRawData` creates command objects from raw data without exposing construction logic.
- **Template Method**: `addCommand` delegates to type-specific methods (`addGameCommand`, `addAckCommand`), enforcing a consistent addition workflow while allowing specialization.

*Not inferable*: Exact memory pool implementation details or threading model.
