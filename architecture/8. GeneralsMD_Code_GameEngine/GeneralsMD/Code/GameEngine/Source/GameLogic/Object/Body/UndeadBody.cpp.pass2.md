# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/UndeadBody.cpp - Enhanced Analysis

## Architectural Role
This file implements the "undead" respawn mechanic, a core gameplay feature where units survive first death with reduced stats. It bridges the damage system (ActiveBody) with behavior modules (SlowDeathBehavior), enabling complex death animations and effects.

## Cross-References
### Incoming
- **Damage System**: `attemptDamage` is called by the game's damage resolution pipeline when units take damage.
- **INI Parsing**: `buildFieldParse` is invoked during module initialization to configure second-life parameters from INI files.
- **Serialization**: `xfer` is called during save/load and network synchronization.

### Outgoing
- **ActiveBody**: Extends base damage handling (`attemptDamage`, `setMaxHealth`, `setArmorSetFlag`).
- **SlowDeathBehavior**: Triggers slow death animations via `beginSlowDeath` after first death.
- **Random System**: Uses `GameLogicRandomValue` for probabilistic slow death behavior selection.

## Design Patterns
- **Template Method**: Extends `ActiveBody` with specialized damage handling while preserving base behavior.
- **Strategy**: Delegates slow death behavior selection to registered `SlowDeathBehaviorInterface` modules.
- **State Pattern**: Implicitly manages "first life" vs. "second life" states via `m_isSecondLife` flag.
