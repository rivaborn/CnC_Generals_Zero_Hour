# GeneralsMD/Code/GameEngine/Include/Common/SpecialPowerType.h - Enhanced Analysis

## Architectural Role
This header defines the core enumeration for special powers/abilities in the game, serving as a central type reference for game logic, UI, and networking subsystems. Its enum values are critical for save/load compatibility and cross-faction power handling.

## Cross-References
### Incoming
- Game logic (e.g., `Unit.cpp`, `Building.cpp`) for power activation
- UI (`HUD.cpp`, `Menu.cpp`) for power display/selection
- Networking (`Replication.cpp`) for power state synchronization
- Scripting (`ScriptEngine.cpp`) for modded power definitions

### Outgoing
- References `SpecialPowerMaskType` (bitmask utilities)
- Relies on `SpecialPower.cpp` for string mappings

## Design Patterns
- **Type Object**: Enum serves as a symbolic constant registry for powers
- **Data-Driven Design**: Powers defined here are instantiated elsewhere (e.g., `GameCore.cpp`)
- **Versioning**: Explicit handling of obsolete powers (e.g., `SPECIAL_DEMORALIZE_OBSOLETE`) for backward compatibility

*Token count: 198*
