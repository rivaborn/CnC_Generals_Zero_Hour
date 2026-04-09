# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SlavedUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core module for managing "slaved" unitsâunits that follow and assist a master unit (e.g., scout drones, repair drones). It integrates with the game's update system and provides a state machine for repair behaviors, making it a key part of the AI and unit behavior pipeline.

## Cross-References
### Incoming
- **MobMemberSlavedUpdate.h**: Inherits and extends `SlavedUpdate`, calling its methods (`doAttackLogic`, `doScoutLogic`, `doRepairLogic`, `onEnslave`, etc.).
- **Other AI/behavior modules**: Likely call `update()` to process slaved unit logic.

### Outgoing
- **UpdateModule.h**: Inherits from `UpdateModule`, using its base functionality.
- **INI.h**: Uses `MultiIniFieldParse` for configuration parsing.
- **DamageInfo, ModelConditionFlagType**: Forward declarations for damage/repair state handling.

## Design Patterns
- **Module Pattern**: Encapsulates slaved behavior as a reusable module, configurable via INI.
- **State Machine**: `RepairStates` enum and `doRepairLogic` implement a state machine for repair sequences (e.g., UNPACKING â WELDING).
- **Observer Pattern**: `onEnslave`, `onSlaverDie`, `onSlaverDamage` act as callbacks for master unit events.
