# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hcanim.h - Enhanced Analysis

## Architectural Role
This header defines the core compressed animation system for the W3D engine, bridging the gap between raw animation data and the hierarchical skeleton system (HTreeClass). It enables efficient storage and retrieval of animated transformations while supporting multiple compression schemes.

## Cross-References
### Incoming
- Animation playback systems (likely in WW3D2)
- Skeleton/rigging systems (HTreeClass users)
- W3D file loading infrastructure

### Outgoing
- W3D file I/O (ChunkLoadClass)
- Motion channel implementations (TimeCodedMotionChannelClass, etc.)
- Math utilities (Vector3, Quaternion, Matrix3D)

## Design Patterns
- **Composite Pattern**: Hierarchy of motion channels (translation/rotation/visibility) organized per node
- **Strategy Pattern**: Multiple motion channel types (time-coded, adaptive delta) can be swapped
- **Resource Management**: Uses RefCountBase for memory tracking (inherited via HAnimClass)

*Not inferable*: Exact relationship with animation blending system or how compression artifacts are handled.
