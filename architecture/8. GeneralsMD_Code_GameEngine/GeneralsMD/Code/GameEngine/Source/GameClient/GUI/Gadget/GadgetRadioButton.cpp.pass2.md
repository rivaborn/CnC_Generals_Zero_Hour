# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetRadioButton.cpp - Enhanced Analysis

## Architectural Role
This file implements the radio button gadget within the SAGE engine's GUI system, handling mutual exclusion logic and input processing. It integrates with the window management system to enforce radio button group behavior across the entire UI hierarchy.

## Cross-References
### Incoming
- Called by UI event handlers when radio button interactions occur
- Used by menu systems for option selection (e.g., game difficulty, faction selection)
- Likely invoked by the main menu and in-game UI screens

### Outgoing
- Calls `TheWindowManager` for window traversal and message dispatch
- Uses `BitTest/BitSet/BitClear` macros from the bit manipulation utilities
- Relies on `GameWindow` methods for state management and hierarchy navigation

## Design Patterns
- **Observer Pattern**: Radio buttons notify their owner via `GBM_SELECTED` messages when state changes
- **Composite Pattern**: Uses recursive traversal (`doRadioUnselect`) to manage hierarchical window relationships
- **Strategy Pattern**: Input and system message handling are separated into distinct functions (`GadgetRadioButtonInput`, `GadgetRadioButtonSystem`)

*Not inferable*: Exact memory management strategy for `RadioButtonData` (manual `delete` suggests ownership by window)
