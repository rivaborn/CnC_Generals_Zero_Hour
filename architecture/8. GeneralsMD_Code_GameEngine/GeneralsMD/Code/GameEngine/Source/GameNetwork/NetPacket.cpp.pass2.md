# GeneralsMD/Code/GameEngine/Source/GameNetwork/NetPacket.cpp - Enhanced Analysis

## Architectural Role
This file is the core of the SAGE engine's network serialization layer, handling the low-level parsing and construction of network packets for all game commands. It bridges the high-level game logic (via NetCommandMsg subclasses) with the raw network transmission layer.

## Cross-References
### Incoming
- GameNetwork/NetCommandMsg.cpp (uses NetPacket for packet construction)
- GameNetwork/NetworkManager.cpp (likely calls packet construction methods)
- GameLogic/CommandSystem.cpp (for game command serialization)

### Outgoing
- GameNetwork/GameMessageParser.cpp (for message-specific parsing)
- GameNetwork/NetworkUtil.cpp (for utility functions)
- Memory management system (via NEW/DELETE macros)

## Design Patterns
- **Factory Pattern**: `ConstructNetCommandMsgFromRawData` acts as a factory for creating different NetCommandMsg subclasses based on packet data.
- **Visitor Pattern**: The command type dispatch in `ConstructNetCommandMsgFromRawData` resembles a visitor pattern for different message types.
- **Builder Pattern**: `ConstructBigCommandPacketList` builds packets incrementally for large commands.

Rules followed. Analysis limited to 400 tokens.
