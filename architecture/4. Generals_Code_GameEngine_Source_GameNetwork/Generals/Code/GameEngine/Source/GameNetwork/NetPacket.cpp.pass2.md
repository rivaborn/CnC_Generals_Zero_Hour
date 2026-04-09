# Generals/Code/GameEngine/Source/GameNetwork/NetPacket.cpp - Enhanced Analysis

## Architectural Role
This file is the core of the SAGE engine's network packet serialization/deserialization system, bridging low-level networking and game logic. It handles packet fragmentation, command parsing, and cross-platform data conversion, making it critical for multiplayer functionality.

## Cross-References
### Incoming
- `GameNetwork/NetCommandMsg.cpp` (uses packet construction/destruction)
- `GameNetwork/NetworkManager.cpp` (sends/receives packets)
- `GameNetwork/GameMessageParser.cpp` (message-specific parsing)

### Outgoing
- `GameNetwork/GameMessageParser.h` (message parsing helpers)
- `GameNetwork/NetworkUtil.h` (utility functions)
- `GameNetwork/NetworkDefs.h` (command type definitions)

## Design Patterns
- **Factory Pattern**: `ConstructNetCommandMsgFromRawData` dynamically creates message objects based on packet content
- **Visitor Pattern**: Message-specific parsers (`readGameMessage`, etc.) act as visitors for packet data
- **Wrapper Pattern**: `NetWrapperCommandMsg` handles fragmented packet reassembly

*Not inferable*: Exact memory management strategy (manual vs. smart pointers)
