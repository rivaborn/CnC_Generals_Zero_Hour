# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CaveContain.h - Enhanced Analysis

## Architectural Role
This file defines the `CaveContain` module, which extends the `OpenContain` behavior to manage cave/tunnel units as specialized containers. It integrates with the `CaveManager` system to handle distributed garrison logic across connected caves, ensuring team changes propagate correctly.

## Cross-References
### Incoming
- **Scripting System**: Calls `tryToSetCaveIndex` for dynamic cave grouping.
- **Damage System**: Invokes `onDie` during destruction.
- **Team System**: Uses `changeTeamOnAllConnectedCaves` for capture propagation.

### Outgoing
- **CaveManager**: Likely queries cave group membership.
- **Team System**: Modifies team ownership for connected caves.
- **Containment System**: Overrides `OpenContain` methods for cave-specific logic.

## Design Patterns
- **Template Method**: Overrides `OpenContain` methods while preserving core behavior.
- **Observer**: Notifies connected caves of team changes (distributed garrison).
- **Strategy**: Delegates containment logic to `CaveManager` for cave-specific rules.
