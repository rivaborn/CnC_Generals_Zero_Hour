# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/RiderChangeContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the specialized transport logic for the "combat bike" unit in Generals/Zero Hour, extending the base `TransportContain` class. It handles the unique behavior where units can switch places on the bike, including model condition changes, weapon set modifications, and experience transfer between rider and vehicle.

## Cross-References
### Incoming
- **AI System**: Calls `getAI()->aiEvacuateInstantly()` during unit boarding
- **Experience System**: Transfers experience via `setVeterancyLevel()`
- **UI System**: Interfaces with `TheInGameUI` and `TheControlBar` for pip display
- **Object System**: Uses `TheThingFactory` for template validation

### Outgoing
- **Transport System**: Extends `TransportContain` base class methods
- **Model System**: Modifies model conditions via `setModelConditionState()`
- **Weapon System**: Adjusts weapon sets through `setWeaponSetFlag()`
- **Status System**: Manages object status flags

## Design Patterns
- **Template Method**: Extends base class methods while preserving core transport behavior
- **Strategy**: Encapsulates rider-specific configurations in `RiderInfo` structs
- **State**: Manages bike scuttling as a timed state transition

*Not inferable*: Exact implementation of experience transfer mechanism or scuttling animation coordination.
