# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/CleanupHazardUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the hazard cleanup behavior for units, bridging the AI system with the weapon/partition systems. It handles both passive cleanup (scanning nearby hazards) and active area cleanup (moving to designated positions while scanning).

## Cross-References
### Incoming
- AIUpdateModule (calls setCleanupAreaParameters for area cleanup commands)
- WeaponSystem (uses weapon templates for range calculations)
- PartitionManager (queries for hazard objects)

### Outgoing
- AIUpdateInterface (aiBusy, aiAttackObject, aiMoveToPosition)
- PartitionManager (getClosestObject with filters)
- WeaponTemplate (getAttackRange)

## Design Patterns
- **Strategy Pattern**: Encapsulates cleanup behavior as a module that can be attached to different unit types
- **Observer Pattern**: Monitors AI state changes to adjust cleanup behavior dynamically
- **State Pattern**: Implicitly manages cleanup states (idle scanning vs active cleanup) through frame counters

Rules followed. Analysis limited to 400 tokens.
