# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SlavedUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the core behavior for slaved units (e.g., scout drones) in the game's object update system. It manages unit positioning, repair logic, and state transitions relative to a master unit, integrating tightly with the AI, locomotion, and damage systems.

## Cross-References
### Incoming
- `MobMemberSlavedUpdate.cpp` calls `doAttackLogic`, `doRepairLogic`, `startSlavedEffects`, `stopSlavedEffects`, and `update` (inheritance relationship)
- Other slaved unit implementations likely depend on this base functionality

### Outgoing
- Calls into `AIUpdateInterface` for movement and behavior commands
- Uses `Locomotor` for pathfinding and positioning
- Interacts with `StealthUpdate` for stealth state management
- Depends on `GameLogic` for object lookup and terrain queries

## Design Patterns
- **Strategy Pattern**: Different behaviors (attack, repair, scout) are encapsulated in separate methods, allowing dynamic selection based on game state
- **State Pattern**: Repair logic uses explicit states (`REPAIRSTATE_NONE`, `REPAIRSTATE_MOVING`, etc.) with clear transitions
- **Observer Pattern**: Reacts to master unit events (damage, death) via callback methods (`onSlaverDie`, `onSlaverDamage`)

*Not inferable*: Exact implementation of command pattern for AI actions (e.g., `CMD_FROM_AI`) would require deeper analysis of `AIUpdateInterface`.
