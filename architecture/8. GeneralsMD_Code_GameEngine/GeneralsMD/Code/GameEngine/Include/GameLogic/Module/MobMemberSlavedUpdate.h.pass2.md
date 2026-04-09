# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MobMemberSlavedUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core AI module for managing "mob" units (e.g., scout drones, stinger soldiers) that follow a master unit. It implements the slaved behavior pattern where units maintain proximity to their master while handling state transitions, damage responses, and visual effects.

## Cross-References
### Incoming
- **AI System**: Uses `SlavedUpdateInterface` for master-slave relationships
- **Damage System**: Handles `DamageInfo` callbacks for slaver death/damage
- **INI System**: Extends `UpdateModuleData` for configuration parsing
- **Thing/Object System**: Operates on `Thing` objects with `ObjectID` references

### Outgoing
- **Effect System**: Calls `startSlavedEffects`/`stopSlavedEffects` (likely W3D effect system)
- **Tasking System**: Manages `isSelfTasking` flag for autonomous behavior
- **Positioning System**: Uses `Coord3D` for spatial calculations
- **Color System**: Manages `RGBColor` for visual differentiation

## Design Patterns
- **State Pattern**: Uses `MobStates` enum to manage different behaviors (idle, catching up, attacking)
- **Observer Pattern**: Implements callbacks (`onEnslave`, `onSlaverDie`) for master lifecycle events
- **Strategy Pattern**: Configurable behavior via `MobMemberSlavedUpdateModuleData` parsed from INI files

*Not inferable*: Exact implementation of catch-up logic or effect system integration.
