# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyWarehouseCripplingBehavior.h - Enhanced Analysis

## Architectural Role
This file defines a behavior module that integrates with the damage and update systems to implement supply warehouse crippling mechanics. It bridges the damage state system with the building functionality, ensuring crippled warehouses lose their supply production capabilities until healed.

## Cross-References
### Incoming
- **DamageModule**: Calls `onDamage()` and `onBodyDamageStateChange()` when damage occurs
- **UpdateModule**: Calls `update()` for periodic healing checks
- **BuildingSystem**: Likely calls `startCrippledEffects()`/`stopCrippledEffects()` to toggle supply production

### Outgoing
- **DamageModuleInterface**: Implements damage response methods
- **UpdateModule**: Inherits update timing functionality
- **BuildingModule**: Calls into building-specific functionality to enable/disable supply production

## Design Patterns
- **Strategy Pattern**: Encapsulates crippling behavior as a module that can be attached to different building types
- **State Pattern**: Manages transitions between damaged/crippled states with different behavior rules
- **Observer Pattern**: Reacts to damage events and state changes from other systems

*Not inferable*: Exact implementation of `startCrippledEffects()`/`stopCrippledEffects()` interaction with building systems.
