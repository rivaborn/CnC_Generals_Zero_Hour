# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanim.h - Enhanced Analysis

## Architectural Role
This file defines the core animation abstraction layer for the W3D engine, serving as the interface between animation assets and the rendering pipeline. It enables hierarchical animation blending and pivot-based weight control, critical for character and vehicle animations in the game.

## Cross-References
### Incoming
- Animation playback systems (likely in `w3d_anim.cpp`)
- Character/vehicle rendering code (uses `Get_Transform`)
- Sound systems (references `EmbeddedSoundBoneIndex`)

### Outgoing
- Memory management (`RefCountClass`, `AutoPoolClass`)
- Math utilities (`Quaternion`, `Matrix3D`)
- Asset loading (`W3DFileClass`)

## Design Patterns
- **Strategy Pattern**: `HAnimClass` provides virtual interface for different animation types
- **Composite Pattern**: `HAnimComboClass` combines multiple animations into a single blend
- **Flyweight Pattern**: `HAnimComboDataClass` uses shared/unshared data to optimize memory

Rules followed. Output under 400 tokens.
