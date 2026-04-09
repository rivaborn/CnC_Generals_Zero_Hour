# Generals/Code/Tools/WorldBuilder/include/WBHeightMap.h - Enhanced Analysis

## Architectural Role
This file defines the WBHeightMap class, which extends the engine's HeightMapRenderObjClass for use in the WorldBuilder editor. It bridges the runtime rendering system (W3D) with the editor's terrain manipulation needs, providing specialized rendering and collision testing for heightmap editing.

## Cross-References
### Incoming
- Likely called by WorldBuilder's terrain editing UI and viewport rendering systems
- May be referenced by WB's terrain tool implementations (e.g., brush tools, elevation tools)

### Outgoing
- Inherits from HeightMapRenderObjClass (W3D rendering system)
- Uses RenderInfoClass and RayCollisionTestClass from the W3D rendering pipeline
- Depends on Coord3D for spatial calculations

## Design Patterns
- **Template Method**: Overrides virtual methods from HeightMapRenderObjClass (Render, Cast_Ray) while maintaining base class behavior
- **State Pattern**: m_drawEntireMap and m_flattenHeights flags suggest runtime behavior modification
- **Adapter**: Converts W3D's generic heightmap interface to editor-specific functionality

*Not inferable: No clear use of Factory, Observer, or Visitor patterns in this header alone.*
