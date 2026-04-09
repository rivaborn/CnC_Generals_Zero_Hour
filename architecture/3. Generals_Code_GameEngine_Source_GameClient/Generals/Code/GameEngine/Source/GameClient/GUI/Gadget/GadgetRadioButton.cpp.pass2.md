# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetRadioButton.cpp - Enhanced Analysis

## Architectural Role
This file implements the radio button GUI control within the SAGE engine's window management system. It handles input, selection logic, and system messaging for radio buttons, ensuring only one button per group can be selected. It integrates with the broader UI framework through the `GameWindowManager` and `GameWindow` classes.

## Cross-References
### Incoming
- **UI System**: Calls from other UI components (e.g., menu systems) to create/modify radio buttons.
- **Input System**: Mouse/keyboard input handlers dispatch messages to `GadgetRadioButtonInput`.
- **Window Manager**: `TheWindowManager` invokes `GadgetRadioButtonSystem` for system messages.

### Outgoing
- **Window Management**: Relies on `GameWindowManager` for message routing and window traversal.
- **Bit Manipulation**: Uses `BitTest`, `BitSet`, `BitClear` for state management.
- **Memory Management**: Directly calls `delete` for `RadioButtonData` cleanup.

## Design Patterns
- **Observer Pattern**: Radio buttons notify owners via `GBM_SELECTED` messages when selected.
- **Composite Pattern**: Recursive traversal of window hierarchy in `doRadioUnselect`.
- **Strategy Pattern**: Input/system message handling is delegated to specialized functions (`GadgetRadioButtonInput`, `GadgetRadioButtonSystem`).

*Not inferable*: No clear use of Factory, Decorator, or Command patterns.
