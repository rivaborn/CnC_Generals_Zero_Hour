# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetCheckBox.cpp - Enhanced Analysis

## Architectural Role
This file implements the checkbox GUI control within the SAGE engine's window management system. It handles user input, state management, and system messaging for checkboxes, integrating with the broader UI framework.

## Cross-References
### Incoming
- Called by window message handlers when processing checkbox-related events
- Likely invoked by UI layout code when creating checkbox controls

### Outgoing
- Calls `TheWindowManager->winSendSystemMsg` extensively to propagate events
- Uses `window->winSetText` for label management
- References `TheWindowManager->winNextTab`/`winPrevTab` for keyboard navigation

## Design Patterns
- **Message Handler Pattern**: Uses message-based communication for input and system events
- **State Management via Bitflags**: Uses bitwise operations on `WIN_STATE_SELECTED` for checked state
- **Event Propagation**: System messages are forwarded to parent windows for higher-level handling

Rules followed. Output under 400 tokens.
