# Generals/Code/Tools/WorldBuilder/src/ScorchOptions.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for scorch mark configuration in WorldBuilder, bridging MFC dialog handling with the game's object property system. It demonstrates the tool's use of undoable operations and property dictionaries for map editing.

## Cross-References
### Incoming
- `CWorldBuilderDoc` calls `ScorchOptions::update()` to refresh UI when selection changes
- `WbView3d` likely triggers updates through selection events
- Other tool dialogs may reference similar patterns for property editing

### Outgoing
- Calls into `MapObject` iteration system for selection queries
- Uses `Dict`/`DictItemUndoable` for property modification with undo support
- Interfaces with `CWorldBuilderDoc` for undo stack management
- Triggers `WbView3d` invalidation for visual updates

## Design Patterns
- **Singleton-like access** via `m_staticThis` for global dialog state
- **Command pattern** through `DictItemUndoable` for property changes
- **Observer pattern** where UI updates in response to selection changes

*Not inferable:* Exact relationship with other property editors (may share common base class)
