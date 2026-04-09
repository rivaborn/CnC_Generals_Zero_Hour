# Generals/Code/Libraries/Source/WWVegas/WW3D2/prim_anim.h - Enhanced Analysis

## Architectural Role
This file defines the core animation system for the W3D rendering engine, providing keyframe-based interpolation for primitive objects. It serves as the foundation for animated visual elements in the game, bridging the gap between static geometry and dynamic in-game effects.

## Cross-References
### Incoming
- Rendering objects (`RingRenderObjClass`, `SphereRenderObjClass`) use this for animation channels
- Animation controllers likely reference `Evaluate()` for runtime interpolation
- Modding tools may call `Save()`/`Load()` for asset serialization

### Outgoing
- Relies on `SimpleDynVecClass` for dynamic keyframe storage
- Uses `ChunkSaveClass`/`ChunkLoadClass` for binary serialization
- Depends on `WRITE_MICRO_CHUNK` macro for chunk-based I/O

## Design Patterns
- **Template Method Pattern**: `PrimitiveAnimationChannelClass` defines the interface for animation evaluation, with `LERPAnimationChannelClass` providing concrete implementation
- **Composite Pattern**: Keyframes are stored in a `SimpleDynVecClass`, allowing hierarchical animation data management
- **Memento Pattern**: Serialization via chunk I/O preserves animation state for save/load operations

*Not inferable*: Specific usage patterns in game logic or AI systems.
