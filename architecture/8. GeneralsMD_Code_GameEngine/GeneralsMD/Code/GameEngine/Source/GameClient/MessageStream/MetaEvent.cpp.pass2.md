# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/MetaEvent.cpp - Enhanced Analysis

## Architectural Role
This file bridges the low-level input system (raw key/mouse events) with the high-level game command system. It acts as a translator layer, converting platform-specific input messages into game-agnostic meta-events that can be processed by the game logic and UI systems.

## Cross-References
### Incoming
- **GameClient/KeyDefs.h**: Uses key definitions for command mappings
- **GameClient/Mouse.h**: References mouse state and drag tolerance
- **GameClient/InGameUI.h**: Interacts with UI for command execution
- **GameLogic/GameLogic.h**: Accesses game state for command validation

### Outgoing
- **Common/MessageStream.h**: Inserts/appends game messages into the stream
- **Common/INI.h**: Parses configuration for command mappings
- **GameClient/GUICallbacks.h**: Triggers UI callbacks for commands
- **GameClient/DebugDisplay.h**: Integrates with debug visualization systems

## Design Patterns
- **Strategy Pattern**: Different command mappings are selected based on input state (key modifiers, mouse buttons)
- **Observer Pattern**: Listens for raw input events and generates higher-level events
- **Singleton Pattern**: Global `TheMetaMap` instance manages command mappings

*Not inferable*: Exact implementation of double-click detection timing.
