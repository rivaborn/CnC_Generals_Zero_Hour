# Generals/Code/Tools/WorldBuilder/include/FenceOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI dialog for fence object configuration in WorldBuilder, bridging the terrain editing tools with the object placement system. It extends the `COptionsPanel` base class to provide a modeless dialog for adjusting fence properties like spacing and offset.

## Cross-References
### Incoming
- Likely called by `WorldHeightMapEdit` or other terrain editing tools when fence objects need configuration
- May be referenced by the main WorldBuilder UI framework for dialog management

### Outgoing
- Uses `TerrainSwatches` for terrain-related UI elements
- Inherits from `COptionsPanel` (part of the WorldBuilder UI system)
- References `MapObject` for object hierarchy management
- Depends on MFC (`CWnd`, `CTreeCtrl`) for dialog implementation

## Design Patterns
- **Singleton-like static access**: Uses static `m_staticThis` pointer for global access to the dialog instance
- **Observer pattern**: `OnNotify` handler suggests event-driven updates to object properties
- **Composite pattern**: Tree view structure (`addObject`, `findOrAdd`) implies hierarchical object organization

*Not inferable*: Exact relationship with `WorldHeightMapEdit` or how fence data persists after dialog closure.
