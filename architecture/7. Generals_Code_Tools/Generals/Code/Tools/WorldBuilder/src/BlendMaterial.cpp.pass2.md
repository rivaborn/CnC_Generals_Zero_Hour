# Generals/Code/Tools/WorldBuilder/src/BlendMaterial.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for terrain texture blending in WorldBuilder, bridging the terrain editing tools with the document model. It manages the presentation layer for blend material selection while coordinating with the underlying heightmap and terrain type systems.

## Cross-References
### Incoming
- `CWorldBuilderDoc` calls `BlendMaterial` methods to update terrain state
- `WorldHeightMapEdit` provides texture class data via static methods
- `TheTerrainTypes` supplies terrain type definitions for UI population

### Outgoing
- Directly manipulates `CWorldBuilderDoc` and `WorldHeightMapEdit` instances
- Uses MFC controls (`CTreeView`, `CDialog`) for UI rendering
- Queries `TheTerrainTypes` for terrain metadata

## Design Patterns
- **Singleton-like** via `m_staticThis` for global dialog access
- **Observer** pattern in `OnNotify` for tree view event handling
- **Composite** in tree view construction (parent-child terrain relationships)

*Not inferable: No clear Factory, Strategy, or Visitor patterns evident.*
