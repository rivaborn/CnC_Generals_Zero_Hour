# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CashHackSpecialPower.h - Enhanced Analysis

## Architectural Role
This file defines the Cash Hack special power module, which is part of the game's special abilities system. It extends the base `SpecialPowerModule` to implement money theft mechanics, integrating with the science/upgrade system and object targeting logic.

## Cross-References
### Incoming
- Likely called by `SpecialPowerModule` subclasses or the power management system when Cash Hack is activated
- May be referenced in modding infrastructure for custom special powers

### Outgoing
- Inherits from `SpecialPowerModule`, using its virtual interface
- Uses `ScienceType` enum for upgrade validation
- Relies on memory pool and module macros from the engine framework

## Design Patterns
- **Template Method**: `doSpecialPowerAtObject`/`doSpecialPowerAtLocation` define hooks for derived behavior
- **Strategy**: Encapsulates Cash Hack logic as a pluggable module in the special power system
- **Composite**: `Upgrades` vector allows dynamic configuration of theft amounts per science level

*Not inferable*: Exact relationship with `FieldParse` or `SpecialPowerTemplate` not visible in header.
