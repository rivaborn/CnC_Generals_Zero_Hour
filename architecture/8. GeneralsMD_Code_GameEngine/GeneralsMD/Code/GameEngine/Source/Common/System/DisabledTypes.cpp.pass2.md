# GeneralsMD/Code/GameEngine/Source/Common/System/DisabledTypes.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central definition and initialization point for disabled state bitmasks used throughout the game logic subsystem. It provides the foundational types and constants that other systems use to track and manipulate entity disabled states.

## Cross-References
### Incoming
- Game logic systems (Unit.cpp, Building.cpp) likely use these masks to check/modify disabled states
- AI subsystem may query disabled states for tactical decisions
- Network code may serialize these masks for synchronization

### Outgoing
- Relies on BitFlagsIO.h for bitmask manipulation utilities
- Uses DisabledTypes.h for type definitions and macros

## Design Patterns
- **Singleton-like initialization**: Global DISABLEDMASK constants act as singletons for disabled state definitions
- **Bitmask pattern**: Uses bit flags to efficiently represent multiple disabled states
- **Serialization support**: s_bitNameList enables serialization/deserialization of disabled states

(Word count: 150)
