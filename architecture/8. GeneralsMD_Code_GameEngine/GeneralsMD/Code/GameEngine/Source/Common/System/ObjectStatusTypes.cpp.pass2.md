# GeneralsMD/Code/GameEngine/Source/Common/System/ObjectStatusTypes.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central registry for object status flags in the SAGE engine, providing a shared bitmask system used across game logic, AI, and rendering subsystems. The status flags here are critical for game state management, affecting unit behavior, collision detection, and visual representation.

## Cross-References
### Incoming
- Game logic files (e.g., `Unit.cpp`, `Building.cpp`) use these status masks to modify object behavior
- AI subsystem references status flags for decision-making (e.g., `CAN_ATTACK`, `STEALTHED`)
- W3D rendering system checks flags like `AFLAME` or `DESTROYED` for visual effects

### Outgoing
- Relies on `BitFlagsIO.h` for serialization of status masks during networking/saving
- No direct outgoing calls - purely data definition

## Design Patterns
- **Registry Pattern**: Centralized definition of all possible status flags
- **Bitmask Enumeration**: Uses bit flags for compact status representation
- **Internationalization Support**: String names suggest potential localization hooks (though not implemented here)

*Not inferable*: No clear use of other patterns from this file alone.
