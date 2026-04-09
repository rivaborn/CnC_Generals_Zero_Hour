# Generals/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.h - Enhanced Analysis

## Architectural Role
This file defines the core animation data structure (`HRawAnimClass`) for the W3D rendering pipeline, bridging between raw animation assets and the hierarchical skeleton system. It encapsulates motion data (translation, rotation, visibility) per node, enabling skeletal animation playback.

## Cross-References
### Incoming
- Animation playback systems (e.g., `HAnimClass` subclasses)
- W3D model loading pipeline (calls `Load_W3D`)
- Rendering systems querying transforms/visibility

### Outgoing
- `MotionChannelClass`/`BitChannelClass` for motion data storage
- `ChunkLoadClass` for W3D file parsing
- `Vector3`/`Quaternion`/`Matrix3D` for transform math

## Design Patterns
- **Composite**: `HRawAnimClass` aggregates `NodeMotionStruct` instances, each holding motion channels.
- **Adapter**: Translates raw W3D animation data into a hierarchical format for the skeleton system.
- **Template Method**: `Load_W3D` orchestrates loading via helper methods (`read_channel`, `add_channel`).
