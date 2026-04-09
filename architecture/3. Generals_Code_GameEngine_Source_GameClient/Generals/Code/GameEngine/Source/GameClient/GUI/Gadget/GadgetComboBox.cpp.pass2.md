# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetComboBox.cpp - Enhanced Analysis

## Architectural Role
This file implements the ComboBox GUI control, acting as a composite gadget that manages three sub-gadgets (edit box, list box, and dropdown button). It bridges the low-level input handling with higher-level UI management through the WindowManager system.

## Cross-References
### Incoming
- Called by UI event handlers (GWM_CHAR, GWM_LEFT_UP) and system messages (GCM_*)
- Used by menu systems and option dialogs for dropdown selections

### Outgoing
- Relies heavily on WindowManager for message routing (winSendSystemMsg, winSendInputMsg)
- Delegates to sub-gadgets (GadgetTextEntry, GadgetListBox, GadgetPushButton)
- Uses AudioEventRTS for sound feedback

## Design Patterns
- **Composite Pattern**: ComboBox contains and manages multiple sub-gadgets
- **Message Passing**: Uses WindowManager's message system for inter-gadget communication
- **Wrapper/Adapter**: Provides convenience functions that delegate to sub-gadgets

*Not inferable*: No clear use of Observer or Strategy patterns in visible code.
