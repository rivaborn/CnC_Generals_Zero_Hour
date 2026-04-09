# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarOCLTimer.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for the On-Construction-List (OCL) timer in the control bar, bridging the game's construction system with the UI rendering pipeline. It handles real-time updates of construction progress and manages context-specific UI elements like the sell button and portrait display.

## Cross-References
### Incoming
- Called by the control bar's context management system when switching to OCL display mode
- Likely invoked by the game's construction update loop (via `updateContextOCLTimer`)

### Outgoing
- Interacts with `OCLUpdate` module for construction progress data
- Uses `GameWindowManager` for UI element access
- Depends on `GameText` for localized string formatting
- Relies on `ControlBar` base class for common UI functionality

## Design Patterns
- **Observer Pattern**: The timer updates only when construction time changes (`m_displayedOCLTimerSeconds` comparison)
- **Dependency Injection**: Receives `Object` reference to query construction state
- **Template Method**: `populateOCLTimer` sets up UI while delegating progress updates to `updateContextOCLTimer`

*Not inferable*: No clear use of Strategy or Factory patterns in this file.
