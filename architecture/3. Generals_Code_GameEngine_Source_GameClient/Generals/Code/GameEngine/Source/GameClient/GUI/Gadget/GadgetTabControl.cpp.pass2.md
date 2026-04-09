# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetTabControl.cpp - Enhanced Analysis

## Architectural Role
This file implements the core logic for the tab control GUI component in the SAGE engine's window management system. It handles input processing, layout calculations, and sub-pane management for tabbed interfaces, which are critical for organizing complex UI screens in the game.

## Cross-References
### Incoming
- **Gadget.h**: Likely registers this gadget type and calls its message handlers
- **GameWindowManager.h**: Uses the window manager to create child windows and send system messages
- **Other GUI gadgets**: May call into this for tab control functionality in composite UI elements

### Outgoing
- **Window Management**: Calls `TheWindowManager` for window creation and message routing
- **Input System**: Processes mouse coordinates from packed input data
- **Child Windows**: Manages sub-panes as child windows with specific positioning logic

## Design Patterns
- **Composite Pattern**: Manages a collection of sub-panes (child windows) as a single tab control unit
- **Strategy Pattern**: Different layout calculations based on tab edge position (top/bottom/left/right)
- **Observer Pattern**: Reacts to system messages (resize, create, destroy) to maintain state

Rules followed. Output under 400 tokens.
