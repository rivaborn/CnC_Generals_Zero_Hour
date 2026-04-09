# GeneralsMD/Code/GameEngine/Source/Common/RTS/ScoreKeeper.cpp - Enhanced Analysis

## Architectural Role
This file implements the `ScoreKeeper` class, which is attached to each player to track game statistics (units built/destroyed, resources, etc.) for scoring. It bridges game events (via `GameLogic`) with the UI (score screen) and persistence (save/load).

## Cross-References
### Incoming
- **GameLogic**: Calls `addObjectBuilt`, `addObjectDestroyed` when objects are created/destroyed
- **UI Systems**: Likely reads `calculateScore` for score display
- **Save/Load**: Calls `xfer` during serialization

### Outgoing
- **GameLogic**: Queries `isScoringEnabled()`
- **ThingFactory**: Resolves templates during deserialization
- **Xfer**: Handles serialization/deserialization

## Design Patterns
- **Observer**: Listens to game events (object creation/destruction) to update stats
- **Strategy**: Uses `KindOfMaskType` for flexible filtering of scorable objects
- **Memento**: Serializes state for save/load via `xfer`

*(Not inferable: No clear use of Visitor, Factory, or Decorator patterns.)*
