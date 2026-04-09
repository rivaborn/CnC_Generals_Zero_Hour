# GeneralsMD/Code/GameEngine/Include/Common/BuildAssistant.h - Enhanced Analysis

## Architectural Role
Central mediator for construction logic, bridging game rules (prerequisites, money) with spatial validation (terrain, pathfinding). Acts as a facade between UI/build commands and core game systems (object creation, pathfinding, player economy).

## Cross-References
### Incoming
- **UI/BuildSystem**: Calls `isLocationLegalToBuild`, `canMakeUnit` for build validation
- **ProductionFacilities**: Uses `canMakeUnit` for queue management
- **PlayerEconomy**: Likely called by money/credit systems for sell operations
- **Pathfinding**: `isLocationClearOfObjects` called by pathfinding subsystem

### Outgoing
- **ObjectCreation**: Calls into object instantiation systems (`buildObjectNow`)
- **Pathfinding**: Uses pathfinding for `CLEAR_PATH` checks
- **TerrainSystem**: Validates terrain restrictions
- **ShroudSystem**: Checks `SHROUD_REVEALED` flag
- **PlayerManager**: Accesses player resources/limits

## Design Patterns
- **Singleton**: `TheBuildAssistant` global instance ensures single authority for build rules
- **Facade**: Hides complexity of terrain/pathfinding/economy checks behind simple APIs
- **Strategy**: `LocalLegalToBuildOptions` bitflags allow dynamic composition of validation rules

*Not inferable*: Exact implementation of `moveObjectsForConstruction` or `clearRemovableForConstruction`
