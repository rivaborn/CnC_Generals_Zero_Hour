# GeneralsMD/Code/GameEngine/Include/Common/ObjectStatusTypes.h - Enhanced Analysis

## Architectural Role
This header defines the core object state management system for the SAGE engine, providing a bitmask-based status system used across game objects for state tracking (e.g., destroyed, stealthed, on fire). It serves as the foundation for object behavior modulation throughout the game logic and rendering systems.

## Cross-References
### Incoming
- Game object classes (e.g., `GameObject`, `Unit`, `Building`) use these status flags for state tracking
- AI systems reference status flags for decision making (e.g., `OBJECT_STATUS_DESTROYED`)
- Rendering systems check flags like `OBJECT_STATUS_AFLAME` for visual effects
- Networking code uses status flags for synchronization (e.g., `OBJECT_STATUS_HIJACKED`)

### Outgoing
- Relies on `BitFlags` template from `Common/BitFlags.h` for bitmask operations
- Uses `BaseType.h` for fundamental types
- References `BitFlagsIO.h` for serialization support

## Design Patterns
- **Type Object Pattern**: The `ObjectStatusMaskType` class encapsulates bitmask operations, providing a clean interface for status flag manipulation.
- **Flag Enumeration**: Uses an enum to define discrete status states, enabling compile-time checking of valid flags.
- **Utility Functions**: Provides inline helper functions for common bitmask operations, promoting consistency in status checks across the codebase.
