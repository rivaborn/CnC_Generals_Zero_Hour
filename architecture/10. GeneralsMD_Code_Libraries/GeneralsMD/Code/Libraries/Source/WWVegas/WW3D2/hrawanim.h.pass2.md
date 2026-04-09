# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.h - Enhanced Analysis

## Architectural Role
This file defines the core animation data structure (`HRawAnimClass`) for the W3D format, bridging the low-level motion channel system with the higher-level animation hierarchy. It serves as the intermediate layer between raw W3D chunk loading and the animation playback system.

## Cross-References
### Incoming
- Animation playback systems (e.g., `HAnimClass` subclasses) likely use this for frame interpolation.
- W3D model loading pipeline calls `Load_W3D` during asset initialization.

### Outgoing
- Directly manipulates `MotionChannelClass` and `BitChannelClass` for motion data storage.
- Relies on `ChunkLoadClass` for W3D file parsing (inherited from `HAnimClass`).

## Design Patterns
- **Composite**: `HRawAnimClass` aggregates `NodeMotionStruct` instances, each containing multiple motion channels.
- **Adapter**: Converts raw W3D chunk data into structured animation data via `Load_W3D` and helper methods.
- **Template Method**: `Load_W3D` orchestrates loading steps (channel reading/addition) with hooks for format-specific handling.
