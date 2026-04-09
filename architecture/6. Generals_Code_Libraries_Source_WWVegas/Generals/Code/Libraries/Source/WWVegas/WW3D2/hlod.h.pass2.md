# Generals/Code/Libraries/Source/WWVegas/WW3D2/hlod.h - Enhanced Analysis

## Architectural Role
This file defines the hierarchical level-of-detail (HLod) system, a core component of the SAGE engine's rendering pipeline. It manages dynamic LOD selection for complex 3D models, integrating with the animation system and scene graph. The HLodClass acts as a container for multiple LOD versions of a model, enabling performance optimization through distance-based rendering.

## Cross-References
### Incoming
- **Rendering System**: Calls into HLodClass::Render() for LOD-based model rendering
- **Animation System**: Uses Animatable3DObjClass interface for animated models
- **Scene Graph**: Integrates via SceneClass notifications (Notify_Added/Removed)
- **Asset Loading**: Called by PrototypeLoaderClass during W3D file loading

### Outgoing
- **W3D Loading**: Uses ChunkLoadClass/ChunkSaveClass for serialization
- **Proxy System**: Interfaces with ProxyArrayClass for modding hooks
- **Bone Hierarchy**: Manages sub-objects via bone indices (Get_Lod_Model_Bone)
- **Snap Points**: Uses SnapPointsClass for attachment points

## Design Patterns
- **Composite Pattern**: HLodClass contains multiple RenderObjClass instances (LOD models) as sub-objects
- **Strategy Pattern**: LOD selection algorithm (Prepare_LOD) encapsulates the decision logic for choosing which model to render
- **Prototype Pattern**: Uses HLodPrototypeClass for object instantiation from definitions (factory pattern variant)

*Not inferable*: Exact LOD selection heuristics (Cost/Value arrays) implementation details.
