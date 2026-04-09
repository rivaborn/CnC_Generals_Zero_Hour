# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/CommandButtonHuntUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the hunting behavior for units, bridging the AI system and the action/command system. It acts as a specialized update module that triggers when units are idle, scanning for valid targets based on command button configurations.

## Cross-References
### Incoming
- **AIUpdateModule**: Calls `huntSpecialPower` when units are idle
- **SpecialAbilityUpdate**: Integrates with special power activation logic
- **ControlBar**: Uses command button configurations to determine hunting behavior

### Outgoing
- **ActionManager**: Validates target actions via `canDoSpecialPowerAtObject`, `canHijackVehicle`, etc.
- **PartitionManager**: Queries spatial partitions for target scanning
- **AIUpdateInterface**: Controls unit state via `aiIdle`

## Design Patterns
- **Strategy Pattern**: Encapsulates different hunting behaviors (special power, weapon, enter) as conditional logic within `scanClosestTarget`
- **Observer Pattern**: Reacts to unit state changes (idle status) to trigger hunting
- **Template Method**: `update()` serves as a template method calling specialized hunting logic

*Not inferable*: Exact pattern usage for command button resolution (e.g., whether it's a factory or registry).
