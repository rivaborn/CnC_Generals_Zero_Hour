# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UnitCrateCollide.h

## Purpose
Defines a crate module that spawns units when picked up by a player.

## Responsibilities
- Inherits from `CrateCollide` to handle crate collision behavior
- Stores unit count and type via `UnitCrateCollideModuleData`
- Implements `executeCrateBehavior` to spawn units on collision
- Provides memory management macros for object pooling

## Key Types
- **UnitCrateCollideModuleData (Class)**: Stores crate configuration (unit count/type)
- **UnitCrateCollide (Class)**: Main crate collision handler
- **UnitCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game entity

## Key Functions
### UnitCrateCollideModuleData::buildFieldParse
- Purpose: Registers INI parsing rules for module data fields
- Calls: `CrateCollideModuleData::buildFieldParse`

### UnitCrateCollide::executeCrateBehavior
- Purpose: Spawns units when crate is picked up
- Calls: Not inferable (implementation in .cpp)

## Globals
None

## Dependencies
- `Common/Module.h` (base module infrastructure)
- `GameLogic/Module/CrateCollide.h` (parent crate collision class)
- `INI` namespace (for field parsing)
- `MultiIniFieldParse` (INI parsing utility)
