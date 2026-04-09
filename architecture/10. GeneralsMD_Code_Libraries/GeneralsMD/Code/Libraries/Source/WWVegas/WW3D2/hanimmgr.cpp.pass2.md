# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.cpp - Enhanced Analysis

## Architectural Role
Central resource manager for hierarchical animations in the W3D rendering pipeline, bridging asset loading with runtime animation playback. Acts as a caching layer between disk-based W3D assets and the real-time animation system.

## Cross-References
### Incoming
- **W3D Model Loading**: Model loading code calls `Load_Anim` during W3D asset parsing
- **Animation Playback**: Game object animation systems call `Get_Anim` to retrieve animations
- **Memory Management**: Engine cleanup systems call `Free_All_Anims` and `Free_All_Anims_With_Exclusion_List`

### Outgoing
- **Animation Subsystems**: Calls into `HAnimClass`, `HRawAnimClass`, `HCompressedAnimClass`, `HMorphAnimClass`
- **Memory System**: Uses `W3DNEW`/`delete` for allocation and `WWMEMLOG` for tracking
- **Chunk I/O**: Uses `ChunkLoadClass` for binary asset parsing

## Design Patterns
- **Resource Pool**: Manages animation assets with reference counting and lazy loading
- **Flyweight**: Shares animation data across multiple game objects via reference counting
- **Null Object**: Uses `MissingAnimTable` to avoid repeated disk lookups for missing assets

*Not inferable*: Specific implementation of compression/decompression for animations.
