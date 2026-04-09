# GeneralsMD/Code/GameEngine/Source/Common/BitFlags.cpp - Enhanced Analysis

## Architectural Role
This file provides the runtime initialization for bit flag enums used throughout the engine for state tracking. The string mappings enable debugging and serialization of game object states across subsystems.

## Cross-References
### Incoming
- **Game Logic**: Unit.cpp, Building.cpp (use ModelConditionFlags for state checks)
- **W3D**: Model.cpp (applies flags for animations/rendering)
- **Network**: Replication.cpp (serializes flag states for multiplayer sync)
- **UI**: HUD.cpp (displays unit states based on flags)

### Outgoing
- **Common**: BitFlagsIO.h (for flag serialization utilities)
- **Game Logic**: ArmorSet.h (for armor state definitions)

## Design Patterns
- **Enum-to-String Mapping**: Provides human-readable names for bitmask debugging
- **Global Initialization**: Static const arrays for runtime flag name lookup
- **Flag-Based State Machine**: Supports composable state tracking across subsystems

(Word count: 150)
