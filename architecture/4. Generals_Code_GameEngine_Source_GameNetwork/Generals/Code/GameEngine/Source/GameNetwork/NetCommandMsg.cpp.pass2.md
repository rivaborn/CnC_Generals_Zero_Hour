# Generals/Code/GameEngine/Source/GameNetwork/NetCommandMsg.cpp - Enhanced Analysis

## Architectural Role
This file implements the core network message system for the SAGE engine, handling serialization/deserialization of game commands, acknowledgments, chat, and file transfers. It bridges the networking layer with game logic by converting network packets into executable GameMessage objects.

## Cross-References
### Incoming
- Networking subsystem (likely NetClient/NetServer) calls constructors and serialization methods
- Game logic (GameMessage handlers) consumes constructed messages
- File transfer system uses NetFileCommandMsg variants

### Outgoing
- Calls into GameState for path conversions (portable â real paths)
- Uses PlayerList/Player for player mask conversions
- Creates GameMessage objects for game command execution

## Design Patterns
- **Reference Counting**: Used for memory management of message objects (attach/detach pattern)
- **Composite**: NetGameCommandMsg maintains a linked list of GameMessageArgument objects
- **Factory Method**: constructGameMessage acts as a factory for creating GameMessage instances

*Not inferable*: Exact networking protocol details or message serialization format.
