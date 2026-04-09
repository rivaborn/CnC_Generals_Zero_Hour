# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SalvageCrateCollide.h - Enhanced Analysis

## Architectural Role
This file defines the salvage crate collision module, extending the base `CrateCollide` system to handle reward distribution (weapons, levels, money) when units interact with salvage crates. It integrates with the game's reward and progression systems, leveraging probability-based logic for dynamic gameplay outcomes.

## Cross-References
### Incoming
- **GameLogic/Module/CrateCollide.h**: Base class for crate collision behavior
- **Common/Module.h**: Core module infrastructure
- **Common/STLTypedefs.h**: Standard type definitions
- **Thing.h**: Game object representation (forward reference)

### Outgoing
- **CrateCollideModuleData::buildFieldParse**: Inherited INI parsing logic
- **INI parsing utilities**: For configuration loading
- **Reward/upgrade systems**: For applying weapon/armor sets and level gains

## Design Patterns
- **Template Method**: `executeCrateBehavior` defines the algorithm skeleton, with hooks like `eligibleForWeaponSet` for subclass customization.
- **Strategy**: Probability-based reward selection (`testWeaponChance`, `testLevelChance`) decouples reward logic from execution.
- **Composite**: Inherits from `CrateCollide`, extending its behavior while reusing base functionality (e.g., INI parsing).

*Not inferable*: Exact reward application mechanisms (e.g., how `doWeaponSet` modifies units).
