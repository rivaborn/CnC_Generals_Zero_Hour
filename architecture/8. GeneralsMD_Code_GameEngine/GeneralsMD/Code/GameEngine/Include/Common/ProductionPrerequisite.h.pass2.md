# GeneralsMD/Code/GameEngine/Include/Common/ProductionPrerequisite.h - Enhanced Analysis

## Architectural Role
This header defines the `ProductionPrerequisite` class, a core component of the game's production system. It bridges the economy/science subsystem (via `Science.h`) with the unit/building template system, enforcing build requirements like tech prerequisites or facility ownership.

## Cross-References
### Incoming
- **Game Logic**: Likely called by `BuildingTemplate` or `UnitTemplate` classes during production checks (e.g., in `canProduce()`).
- **UI**: Possibly referenced by the control bar or build menu to gray out unavailable options.
- **AI**: Used by the AI production planner to determine feasible build paths.

### Outgoing
- **Template System**: Relies on `ThingTemplate` resolution (via `resolveNames()`).
- **Player State**: Queries `Player` for owned units/sciences in `isSatisfied()`.
- **Science System**: Uses `ScienceVec` for tech prerequisites.

## Design Patterns
- **Composite**: Aggregates multiple prerequisites (units/sciences) into a single satisfaction check.
- **Strategy**: Encapsulates prerequisite logic, allowing different templates to define custom rules.
- **Lazy Initialization**: `resolveNames()` defers name-to-template mapping until templates are loaded.
