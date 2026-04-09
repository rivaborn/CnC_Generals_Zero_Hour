# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SalvageCrateCollide.h

## Purpose
Defines the salvage crate collision module, handling weapon/armor upgrades, level gains, and money rewards when units interact with salvage crates.

## Responsibilities
- Manages salvage crate behavior logic
- Handles probability-based rewards (weapons, levels, money)
- Validates eligibility for different reward types
- Parses configuration data from INI files

## Key Types
- **SalvageCrateCollideModuleData (Class)**: Holds configuration data for salvage crate probabilities and money ranges
- **SalvageCrateCollide (Class)**: Implements the salvage crate collision behavior
- **SalvageCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object type

## Key Functions
### SalvageCrateCollideModuleData::buildFieldParse
- Purpose: Registers INI field parsers for salvage crate configuration
- Calls: CrateCollideModuleData::buildFieldParse

### SalvageCrateCollide::isValidToExecute
- Purpose: Determines if the crate behavior can execute for a given object
- Calls: Not inferable

### SalvageCrateCollide::executeCrateBehavior
- Purpose: Executes the main salvage crate behavior logic
- Calls: Not inferable

### SalvageCrateCollide::eligibleForWeaponSet
- Purpose: Checks if object qualifies for weapon upgrades
- Calls: Not inferable

### SalvageCrateCollide::doWeaponSet
- Purpose: Applies weapon upgrade to the object
- Calls: Not inferable

## Globals
None

## Dependencies
- Common/Module.h
- Common/STLTypedefs.h
- GameLogic/Module
