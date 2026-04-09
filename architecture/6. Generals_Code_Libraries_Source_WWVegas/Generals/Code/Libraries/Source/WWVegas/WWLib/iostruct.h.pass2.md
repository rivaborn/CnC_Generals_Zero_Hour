# Generals/Code/Libraries/Source/WWVegas/WWLib/iostruct.h - Enhanced Analysis

## Architectural Role
This file defines the foundational I/O structures used across the engine for serialization of geometric and transform data. It serves as the binary layout contract between the game's runtime data and persistent storage (e.g., save games, map files).

## Cross-References
### Incoming
- **WW3D2 subsystem**: Uses these structures for model/animation serialization (e.g., in `model.cpp`, `anim.cpp`)
- **Game Logic**: Likely referenced in mission/save file I/O (e.g., `mission.cpp`, `savegame.cpp`)
- **Modding Infrastructure**: Used by mod tools for asset serialization

### Outgoing
- **WWLib**: Depends on `bittype.h` for `float32` definition (type consistency)

## Design Patterns
- **Data Transfer Object (DTO)**: Structures are purely data containers for serialization
- **Fixed Layout**: Explicit `float32` usage ensures binary compatibility across platforms
- **Not inferable**: No behavioral patterns (no methods, just data)

*Token count: 198*
