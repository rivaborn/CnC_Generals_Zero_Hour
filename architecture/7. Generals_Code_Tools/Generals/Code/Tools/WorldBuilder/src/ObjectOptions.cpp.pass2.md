# Generals/Code/Tools/WorldBuilder/src/ObjectOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for object manipulation in WorldBuilder, bridging the gap between the editor's visual hierarchy and the underlying map object system. It manages object selection, property editing, and team assignment while coordinating with the game's template and player systems.

## Cross-References
### Incoming
- Called by WorldBuilder's main document/editor framework when objects are selected or modified
- Used by the tree view control for object navigation
- Referenced by the placement/duplication workflow

### Outgoing
- Queries `TheSidesList` for team/player data
- Uses `ThingTemplate` and `ThingFactory` for object metadata
- Interacts with `WorldBuilderDoc` for map object persistence
- Leverages `CUndoable` for command pattern implementation

## Design Patterns
- **Singleton** (`m_staticThis`) for global dialog access across the editor
- **Observer** pattern for UI updates via `updateLabel()` and `update()`
- **Composite** structure for organizing objects in the tree view hierarchy

*Not inferable:* Exact command pattern implementation with `CUndoable` (truncated).
