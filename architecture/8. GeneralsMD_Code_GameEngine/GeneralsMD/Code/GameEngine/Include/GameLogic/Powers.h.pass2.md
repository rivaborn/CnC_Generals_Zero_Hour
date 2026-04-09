# GeneralsMD/Code/GameEngine/Include/GameLogic/Powers.h - Enhanced Analysis

## Architectural Role
This header defines the core power system enums and bit flags used across the game logic subsystem. It serves as a foundational type definition for unit abilities that are referenced by AI, unit behavior, and networking systems.

## Cross-References
### Incoming
- `Unit.cpp` (uses power flags for unit capabilities)
- `AI.cpp` (references power types for behavior decisions)
- `ScriptEngine.cpp` (uses power names for scripting)

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Bit Flag Enum**: Uses bit flags for power combinations (allows multiple powers per unit)
- **Conditional Compilation**: `DEFINE_POWER_NAMES` guard for debug/scripting purposes
- **Type Safety**: Enum values kept in sync with `PowerNames` array for consistency

*Not inferable*: No other patterns clearly visible from this header alone.
