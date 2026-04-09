# Generals/Code/Tools/WorldBuilder/src/TeamBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for team behavior configuration in WorldBuilder, bridging the gap between the editor's property page system and the underlying team data model. It handles serialization of team behavior settings to/from the team dictionary, enforcing business rules like mutual exclusivity of defense modes.

## Cross-References
### Incoming
- Called by MFC framework for property page lifecycle events (OnInitDialog, message handlers)
- Used by WorldBuilder's property page system to manage team behavior UI

### Outgoing
- Calls into `EditParameter` for script loading
- Interacts with `m_teamDict` (team dictionary) for data persistence
- References AI constants from `GameLogic/AI.h` for aggressiveness levels

## Design Patterns
- **Property Page Pattern**: Uses MFC's property page framework to encapsulate team behavior configuration
- **Data Binding**: Binds UI controls to underlying team dictionary values via `setupScript`/`updateScript`
- **Mutual Exclusion Enforcement**: Explicitly prevents simultaneous selection of base/perimeter defense modes
