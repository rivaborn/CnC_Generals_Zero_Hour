# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshbuild.h - Enhanced Analysis

## Architectural Role
This file defines the core mesh processing infrastructure for the SAGE engine's 3D rendering pipeline. It bridges between raw geometry data and optimized renderable meshes, handling vertex/face processing, material organization, and strip optimization critical for the engine's performance-oriented design.

## Cross-References
### Incoming
- **W3D Model Loading**: Model importers (e.g., `.w3d` loader) use `MeshBuilderClass` to process imported mesh data
- **Animation System**: Skinning/animation code likely calls `Build_Mesh` for processed vertex data
- **Shader System**: Shader material assignment uses `MeshStatsStruct` for pass/stage organization

### Outgoing
- **Math Library**: Uses `Vector2`, `Vector3` for geometric calculations
- **Rendering Pipeline**: Output feeds into `WW3D2` renderer's draw calls
- **Collision System**: Bounding volume data likely consumed by physics/collision subsystems

## Design Patterns
- **Strategy Pattern**: `WorldInfoClass` abstract base allows different world info implementations (e.g., terrain vs. unit meshes)
- **Builder Pattern**: `MeshBuilderClass` encapsulates complex mesh construction steps behind a simple interface
- **Composite Pattern**: Hierarchical organization of vertices/faces with shared attributes (e.g., smoothing groups)

*Not inferable*: Exact usage of `WingedEdgeStruct` for strip optimization details.
