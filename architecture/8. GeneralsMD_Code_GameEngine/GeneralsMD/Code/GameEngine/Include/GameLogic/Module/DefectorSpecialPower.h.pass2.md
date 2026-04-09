# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DefectorSpecialPower.h - Enhanced Analysis

## Architectural Role
This file defines the Defector special power module, a key part of the game's special abilities system. It extends the base `SpecialPowerModule` to implement the defect mechanic, where a player can convert enemy units to their side.

## Cross-References
### Incoming
- Likely called by the `SpecialPowerModule` manager when the defect ability is activated.
- May be referenced by UI systems handling ability selection.

### Outgoing
- Inherits from `SpecialPowerModule`, so it calls into the base class's methods.
- Uses `Thing` and `Object` classes for target handling.

## Design Patterns
- **Template Method Pattern**: The `doSpecialPowerAtObject` and `doSpecialPowerAtLocation` methods are virtual, allowing subclasses to override behavior while maintaining a consistent interface.
- **Module Pattern**: The file follows the engine's module-based architecture, with `DefectorSpecialPowerModuleData` providing configuration and `DefectorSpecialPower` implementing the logic.
- **Memory Pool Pattern**: Uses `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE` for object allocation, typical of the SAGE engine's memory management.
