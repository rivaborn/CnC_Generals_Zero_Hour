# Generals/Code/Tools/WorldBuilder/src/teamsdialog.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for team management in WorldBuilder, bridging MFC dialog framework with the game's team/side data model. It handles team creation, validation, and reordering while maintaining synchronization between the UI and underlying `SidesList` data structure.

## Cross-References
### Incoming
- **WorldBuilderDoc**: Likely instantiates `CTeamsDialog` and passes `SidesList` data
- **CFixTeamOwnerDialog**: Called when team ownership validation fails
- **TeamIdentity/TeamReinforcement/TeamBehavior**: Used for team property editing

### Outgoing
- **SidesList**: Core data structure for teams/sides, heavily modified here
- **Dict**: Used for team property serialization
- **MapObject**: For team member selection functionality
- **CUndoable**: For undo/redo support (via `SidesListUndoable`)

## Design Patterns
- **Mediator**: `CTeamsDialog` coordinates between UI controls and `SidesList`
- **Strategy**: Team property editing uses different dialog classes (identity/reinforcement/behavior)
- **Observer**: UI updates via `updateUI()` when underlying data changes

*Not inferable*: Exact undo/redo implementation details (likely Command pattern but not explicitly shown).
