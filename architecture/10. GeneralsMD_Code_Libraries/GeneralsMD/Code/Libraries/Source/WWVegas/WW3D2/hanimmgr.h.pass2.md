# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.h - Enhanced Analysis

## Architectural Role
Central resource manager for hierarchical animation assets in the W3D rendering pipeline, bridging asset loading infrastructure with runtime animation playback systems.

## Cross-References
### Incoming
- `W3DModelClass` (model loading)
- `W3DAnimationControllerClass` (animation playback)
- `W3DSceneClass` (scene composition)

### Outgoing
- `ChunkLoadClass` (asset loading)
- `W3DExclusionListClass` (memory management)
- `HAnimClass` (animation data)

## Design Patterns
- **Resource Pool**: Manages animation assets with load/unload tracking
- **Flyweight**: Shares animation data across multiple model instances
- **Null Object**: `MissingAnimClass` handles failed loads gracefully

*Not inferable: No clear use of Observer or Factory patterns*
