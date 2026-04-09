# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hlod.cpp - Enhanced Analysis

## Architectural Role
This file implements the core HLOD (Hierarchical Level of Detail) system, serving as the bridge between the W3D asset pipeline and runtime rendering. It manages hierarchical model structures, LOD transitions, and proxy object handling, critical for performance optimization in large-scale scenes.

## Cross-References
### Incoming
- **Rendering System**: Calls into `RenderObjClass` methods for model rendering and decal management
- **Animation System**: Uses `Animatable3DObjClass` for base animation functionality
- **Scene Graph**: Interacts with scene management via `Notify_Added`/`Notify_Removed`
- **Asset Pipeline**: Loads/saves W3D assets via `AssetMgrClass` and `ChunkIO`

### Outgoing
- **Hierarchy System**: Depends on `HTreeClass` for bone transformations and pivot management
- **Collision System**: Uses `SphereClass` and `AABoxClass` for bounding volume calculations
- **Particle System**: Special handling for `PARTICLEEMITTER` objects in `Set_Hidden`

## Design Patterns
- **Composite Pattern**: HLODs contain sub-objects (models) that can themselves be HLODs, enabling recursive hierarchy
- **Proxy Pattern**: Uses `ProxyRecordClass` to defer loading of complex sub-objects until needed
- **Observer Pattern**: Notifies sub-objects of scene graph changes via `Notify_Added`/`Notify_Removed` callbacks

*Not inferable*: Exact implementation of LOD selection algorithm (cost-value arrays suggest dynamic LOD management)
