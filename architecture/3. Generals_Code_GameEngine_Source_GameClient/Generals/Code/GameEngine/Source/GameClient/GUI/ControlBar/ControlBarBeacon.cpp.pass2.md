# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarBeacon.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the control bar beacon system, bridging the game's object system with the in-game UI. It handles dynamic UI updates based on object state and input routing for beacon-related windows.

## Cross-References
### Incoming
- `ControlBar.h` (parent class)
- `InGameUI.h` (for input handling)
- `GameWindow.h` (UI window management)

### Outgoing
- `ControlBar::setPortraitByObject` (internal)
- `GadgetTextEntrySetText` (UI text control)
- `TheWindowManager` (global UI manager)
- `TheInGameUI` (global UI controller)

## Design Patterns
- **Observer Pattern**: `populateBeacon` reacts to object state changes (e.g., `isLocallyControlled()`) to update UI.
- **Command Pattern**: `BeaconWindowInput` delegates ESC key handling to `deselectAllDrawables`.
- **NameKey Lookup**: Uses `NAMEKEY` for localized UI element identification (internationalization support).

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
