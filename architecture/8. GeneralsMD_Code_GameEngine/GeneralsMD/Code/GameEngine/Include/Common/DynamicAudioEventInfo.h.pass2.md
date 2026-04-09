# GeneralsMD/Code/GameEngine/Include/Common/DynamicAudioEventInfo.h - Enhanced Analysis

## Architectural Role
This file defines a runtime-customizable audio event system, bridging static INI-based audio definitions with dynamic game logic. It enables the audio subsystem to modify properties like volume, range, and priority without altering base data, critical for contextual audio (e.g., unit-specific sounds, environmental effects).

## Cross-References
### Incoming
- **Audio Subsystem**: Likely called by audio managers to retrieve overridden event properties.
- **Game Logic**: Units/weapons may instantiate `DynamicAudioEventInfo` to customize playback.
- **Serialization**: `Xfer`-related code uses `xferNoName` for save/load.

### Outgoing
- **Base Class**: Directly modifies `AudioEventInfo` fields (inheritance).
- **Memory Management**: Uses `MEMORY_POOL_GLUE` for allocation tracking.
- **String Handling**: Relies on `AsciiString` for name storage.

## Design Patterns
- **Decorator Pattern**: Dynamically wraps `AudioEventInfo` to add override behavior without modifying the base class.
- **State Tracking**: Uses `BitFlags` to explicitly track which fields are overridden, enabling selective serialization.
- **Immutable Base**: Notes suggest `AudioEventInfo` should be immutable (only "get" methods), implying a failed attempt at encapsulation.
