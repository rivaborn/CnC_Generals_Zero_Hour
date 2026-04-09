# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CashBountyPower.h - Enhanced Analysis

## Architectural Role
This file defines the cash bounty power module, part of the game's special power system. It extends the `SpecialPowerModule` base class to provide financial rewards, integrating with the game's economy and module systems.

## Cross-References
### Incoming
- Likely called by `SpecialPowerModule` subclasses or the power activation system
- May be referenced in player economy or reward systems

### Outgoing
- Calls into `SpecialPowerModule` base class methods
- Uses `MultiIniFieldParse` for configuration parsing
- Relies on `Thing` and `Player` for game object interactions

## Design Patterns
- **Template Method**: Extends `SpecialPowerModule` with overridden virtual methods
- **Module Pattern**: Encapsulates cash bounty logic as a self-contained module
- **Dependency Injection**: Receives `ModuleData` through constructor

*Not inferable*: Exact bounty calculation logic or upgrade system usage.
