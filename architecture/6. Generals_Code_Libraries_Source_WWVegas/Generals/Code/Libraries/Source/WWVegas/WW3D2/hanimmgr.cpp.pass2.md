# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanimmgr.cpp - Enhanced Analysis

## Architectural Role
Central resource manager for hierarchical animations in the W3D rendering pipeline, bridging asset loading with runtime animation playback. Acts as a caching layer between disk-based W3D assets and the animation system used by game objects and cutscenes.

## Cross-References
### Incoming
- **Animation playback systems**: Likely called by object rendering/animation update loops
- **Level loading**: Invoked during W3D model asset loading
- **Cutscene system**: Used for scripted animation sequences
- **Modding infrastructure**: Called by mod asset loaders

### Outgoing
- **W3D asset loading**: Uses ChunkLoadClass for file I/O
- **Memory management**: Interfaces with WWMemLog for tracking
- **Animation types**: Instantiates HAnimClass derivatives (HRawAnimClass, HCAnimClass, HMorphAnimClass)
- **Exclusion lists**: Uses W3DExclusionListClass for memory management

## Design Patterns
- **Resource Pool**: Manages animation assets with reference counting
- **Flyweight**: Shares animation data across multiple instances
- **Lazy Initialization**: Loads animations only when requested via Get_Anim
- **Null Object**: Tracks missing animations to avoid repeated disk access

*Not inferable*: Exact relationship with animation blending system or how animations are bound to skeletons.
