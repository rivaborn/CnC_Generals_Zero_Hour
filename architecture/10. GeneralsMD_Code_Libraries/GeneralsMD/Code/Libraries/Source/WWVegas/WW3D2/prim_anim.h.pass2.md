# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/prim_anim.h - Enhanced Analysis

## Architectural Role
This file defines the core animation system for primitive 3D objects in the SAGE engine, enabling keyframe-based animation with linear interpolation. It serves as the foundation for animating properties like position, scale, and color in the rendering pipeline.

## Cross-References
### Incoming
- Rendering objects (`RingRenderObjClass`, `SphereRenderObjClass`) use this for animated properties
- Animation controllers likely reference `Evaluate()` for runtime value computation
- Serialization system calls `Save()`/`Load()` during map/asset loading

### Outgoing
- Relies on `ChunkSaveClass`/`ChunkLoadClass` for binary serialization
- Uses `SimpleDynVecClass` for dynamic keyframe storage
- Depends on `WRITE_MICRO_CHUNK` macro for chunk-based I/O

## Design Patterns
- **Template Method Pattern**: `PrimitiveAnimationChannelClass` defines interface for `Evaluate()`, with `LERPAnimationChannelClass` providing concrete implementation
- **Composite Pattern**: Keyframes stored in `SimpleDynVecClass` allow hierarchical animation data management
- **Memento Pattern**: Serialization via chunk system enables save/load of animation state (implicit)
