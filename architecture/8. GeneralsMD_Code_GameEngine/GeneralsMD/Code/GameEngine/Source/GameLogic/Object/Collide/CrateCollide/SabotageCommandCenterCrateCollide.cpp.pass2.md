# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageCommandCenterCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the sabotage behavior for crates targeting command centers, extending the base `CrateCollide` class. It integrates with the AI system, special power management, and feedback systems to handle enemy command center sabotage mechanics.

## Cross-References
### Incoming
- **AIUpdateInterface**: Validates goal object alignment during sabotage execution
- **SpecialPowerModuleInterface**: Resets special power timers on command centers
- **Radar**: Triggers infiltration events via `TheRadar->tryInfiltrationEvent`
- **Eva**: Plays sabotage announcement via `TheEva->setShouldPlay`

### Outgoing
- **CrateCollide**: Base class for collision behavior (inheritance)
- **Object**: Target validation (relationship checks, death state)
- **BehaviorModule**: Iterates modules to find special power interfaces

## Design Patterns
- **Template Method**: Extends `CrateCollide` methods while preserving base behavior
- **Strategy**: Encapsulates sabotage logic as a module for command centers
- **Observer**: Triggers radar/EVA events as side effects of sabotage

*Not inferable*: No clear use of Visitor, Factory, or Decorator patterns.
