# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation system for the W3D engine, handling hierarchical skeletal animations. It bridges between the low-level chunk-based file I/O system and the higher-level animation playback system, providing interpolated transform data for rendering animated models.

## Cross-References
### Incoming
- Animation playback systems (likely in rendering or model management)
- Hierarchy node processing (htree.h integration)
- Asset management system (assetmgr.h)

### Outgoing
- Chunk I/O system (chunkio.h) for file loading
- Motion channel system (motchan.h) for animation data storage
- Math utilities (WWMath) for interpolation
- Memory management (W3DNEW/W3DNEWARRAY)

## Design Patterns
- **Resource Management**: Uses explicit allocation/deallocation with Free() pattern
- **Composite**: NodeMotionStruct acts as a composite of different motion channels
- **Strategy**: Different motion channels (translation/rotation/visibility) implement similar interfaces but with different data

Key insight: The animation system uses frame interpolation (Lerp for translation, Slerp for rotation) to achieve smooth playback, with visibility handled as discrete bit channels. The design separates motion data storage from playback logic, allowing for efficient memory usage and flexible animation control.
