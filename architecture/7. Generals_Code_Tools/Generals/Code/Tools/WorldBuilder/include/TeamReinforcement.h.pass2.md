# Generals/Code/Tools/WorldBuilder/include/TeamReinforcement.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for team reinforcement configuration in WorldBuilder, bridging the MFC dialog framework with the game's data model (Dict). It's part of the toolchain's property page system for map editing.

## Cross-References
### Incoming
- Likely called by `CPropertySheet`-derived classes in WorldBuilder's main tool window
- `Dict`-based serialization system for saving/loading reinforcement data

### Outgoing
- Uses MFC's `CPropertyPage` base class and DDX/DDV mechanisms
- Interacts with `Dict` for data storage (set via `setTeamDict`)

## Design Patterns
- **Property Page Pattern**: Encapsulates reinforcement settings in a reusable dialog
- **Data Transfer Object**: Uses `Dict` as an external data container (not inferable why, but common in toolchain)
- **Event-Driven UI**: Message handlers for combo box changes and button clicks (MFC idiom)

*Not inferable*: No clear strategy pattern for reinforcement logic; likely delegated to game runtime.
