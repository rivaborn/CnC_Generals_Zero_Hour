# GeneralsMD/Code/GameEngine/Include/GameLogic/ObjectScriptStatusBits.h - Enhanced Analysis

## Architectural Role
This header defines script-controlled object state flags used throughout the game logic subsystem. It serves as a central registry for bitmask values that modify object behavior dynamically via scripting.

## Cross-References
### Incoming
- `Object.h` (uses these bits in object state tracking)
- `ScriptEngine.cpp` (applies status bits via script commands)
- `GameLogic/Object/Unit.cpp` (checks status bits for behavior rules)

### Outgoing
- None (pure enum declaration, no external dependencies)

## Design Patterns
- **Bitmask Flag Pattern**: Uses enum values as bit flags for compact state representation
- **Header Detangling**: Follows modular include strategy (explicit `#pragma once`)
- **Documentation-Driven Design**: Each flag has clear purpose documentation for modders

**Key Insight**: The 8-bit limit warning suggests this was a known constraint in the original architecture, likely due to memory optimization in the SAGE engine's object representation.
