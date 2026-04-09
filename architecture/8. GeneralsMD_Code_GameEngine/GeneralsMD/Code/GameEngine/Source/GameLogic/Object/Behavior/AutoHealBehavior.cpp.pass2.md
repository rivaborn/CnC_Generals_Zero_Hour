# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/AutoHealBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the healing system's behavior module, bridging the game logic layer with rendering (particles/animations) and spatial queries (partition manager). It handles both self-healing and AoE healing mechanics, integrating tightly with the update system and damage event pipeline.

## Cross-References
### Incoming
- **GameLogic/Object.h**: Calls `onDamage` and `update` via the object's module system
- **GameClient/InGameUI.h**: Uses `addWorldAnimation` for visual feedback
- **GameLogic/PartitionManager.h**: Queries objects via `iterateObjectsInRange`

### Outgoing
- **GameClient/ParticleSys.h**: Creates/destroys particle systems for visual effects
- **GameLogic/Module/BodyModule.h**: Checks health status via `getHealth`/`getMaxHealth`
- **Common/Player.h**: Validates target ownership via `getControllingPlayer`

## Design Patterns
- **Strategy Pattern**: Healing logic varies based on configuration (self/radius/player-wide) without changing core behavior
- **Observer Pattern**: Reacts to damage events via `onDamage` to reset healing timers
- **Visitor Pattern**: Uses `checkForAutoHeal` as a callback for spatial queries (partition manager iteration)

*Not inferable*: No clear use of Command or State patterns despite healing state changes.
