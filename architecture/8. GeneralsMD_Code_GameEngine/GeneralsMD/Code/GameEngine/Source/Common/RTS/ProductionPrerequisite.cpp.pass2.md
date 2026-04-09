# GeneralsMD/Code/GameEngine/Source/Common/RTS/ProductionPrerequisite.cpp - Enhanced Analysis

## Architectural Role
This file implements the production prerequisite system, which is central to the game's economy and tech tree. It bridges the gap between unit templates and player state, enabling the game to enforce build requirements dynamically.

## Cross-References
### Incoming
- **Buildable objects**: Call `isSatisfied` to check if production is allowed
- **UI systems**: Call `getRequiresList` to display missing prerequisites
- **Game rules**: Call `addUnitPrereq` during rule initialization

### Outgoing
- **ThingFactory**: For template resolution via `findTemplate`
- **Player**: For science checks and unit counting
- **GameText**: For localized prerequisite descriptions

## Design Patterns
- **Composite**: Groups unit prerequisites into logical blocks (AND/OR relationships)
- **Strategy**: Encapsulates prerequisite checking logic for different resource types
- **Observer (implicit)**: Notifies UI when prerequisites change (via `getRequiresList`)

*Not inferable*: No clear use of Factory, Visitor, or Decorator patterns.
