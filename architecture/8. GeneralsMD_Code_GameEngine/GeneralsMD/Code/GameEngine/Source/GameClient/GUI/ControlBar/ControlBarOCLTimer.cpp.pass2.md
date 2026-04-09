# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarOCLTimer.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the On-Construction-List (OCL) timer in the control bar, bridging between the game's object system and the UI rendering pipeline. It handles the dynamic display of construction timers, button states, and object portraits based on the current selected object's construction status.

## Cross-References
### Incoming
- Called by `ControlBar` context management code when switching to OCL timer display
- Used by `ControlBar` update loop for periodic timer refreshes
- Referenced by `ControlBar` command button handling system

### Outgoing
- Calls into `GameWindowManager` for UI element lookup
- Uses `GameText` for localized string formatting
- Interacts with `OCLUpdate` module for timer data
- Invokes `ControlBar` helper methods like `findCommandButton` and `setPortraitByObject`

## Design Patterns
- **Context Object Pattern**: The file implements context-specific UI behavior for the OCL timer state
- **Observer Pattern**: Periodically checks `OCLUpdate` module for state changes to trigger UI updates
- **Strategy Pattern**: Different button configurations (sell/rally) based on object type (tech building vs. regular building)

*Not inferable*: Exact pattern usage for rally point display management.
