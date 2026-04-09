# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/light.h - Enhanced Analysis

## Architectural Role
This file defines the core lighting system for the SAGE engine, bridging rendering and scene management. It implements vertex processing for lights, integrating with the scene graph and W3D serialization pipeline.

## Cross-References
### Incoming
- Rendering pipeline (calls `Is_Vertex_Processor`, `Render`)
- Scene graph (calls `Notify_Added`, `Notify_Removed`)
- Bounding volume queries (calls `Get_Obj_Space_Bounding_Sphere/Box`)
- W3D serialization (calls `Load_W3D`, `Save_W3D`)

### Outgoing
- Scene management (`SceneClass` registration)
- Math utilities (`WWMath::Fast_Cos`)
- Persistence system (`ChunkLoadClass`, `ChunkSaveClass`)

## Design Patterns
- **Strategy Pattern**: Light behavior varies by type (POINT/DIRECTIONAL/SPOT), with type-specific logic delegated to derived implementations.
- **Observer Pattern**: Lights notify the scene graph of their addition/removal via `Notify_Added/Removed`.
- **Composite Pattern**: Lights are part of the scene graph hierarchy as `RenderObjClass` derivatives.
