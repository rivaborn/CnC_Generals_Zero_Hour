# GeneralsMD/Code/GameEngine/Include/GameClient/MetaEvent.h - Enhanced Analysis

## Architectural Role
This file defines the input mapping system for the SAGE engine, bridging low-level input events (keys/mouse) with high-level game commands. It serves as the central registry for key bindings and their translation into game-specific actions, enabling both default and user-customizable controls.

## Cross-References
### Incoming
- **Input System**: Likely called by the input subsystem to translate raw key/mouse events into game commands
- **UI System**: Used by in-game UI to handle keyboard shortcuts and command bindings
- **Game Logic**: Accessed by game state handlers to determine which commands are available in current context

### Outgoing
- **INI Parser**: Calls `parseMetaMap` to load key bindings from configuration files
- **Game Message System**: Generates `GameMessage` objects for command execution
- **Memory Management**: Uses `MemoryPoolObject` for `MetaMapRec` allocation

## Design Patterns
- **Registry Pattern**: `MetaMap` maintains a linked list of `MetaMapRec` objects, acting as a centralized lookup for key bindings
- **Strategy Pattern**: `MetaEventTranslator` implements `GameMessageTranslator` to convert input events into game-specific actions
- **Lookup Table Pattern**: Uses static arrays (`CategoryListName`, `KeyNames`) for efficient name-to-enum conversions

**Not inferable**: Exact implementation of `translateGameMessage` or how `CommandUsableInType` filters are applied.
