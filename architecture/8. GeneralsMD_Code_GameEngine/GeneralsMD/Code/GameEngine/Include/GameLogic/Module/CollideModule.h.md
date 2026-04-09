# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CollideModule.h

## Purpose
Defines the collision handling module interface and implementation for game objects in the SAGE engine.

## Responsibilities
- Declares the `CollideModuleInterface` for collision responses
- Provides base `CollideModule` class implementing the interface
- Defines module data structure and memory management macros
- Specifies collision-related query methods (e.g., crate types, railroad)

## Key Types
- **CollideModuleInterface (Class)**: Abstract interface for collision behavior
- **CollideModuleData (Class)**: Module data extending `BehaviorModuleData`
- **CollideModule (Class)**: Concrete module implementing collision logic
- **CollideModuleMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **CollideModule_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### `onCollide`
- Purpose: Handles collision events with other objects or terrain
- Calls: None (pure virtual)

### `wouldLikeToCollideWith`
- Purpose: Determines if object wants to collide with another
- Calls: None

### `isHijackedVehicleCrateCollide`
- Purpose: Checks if collision involves a hijacked vehicle crate
- Calls: None

### `isSabotageBuildingCrateCollide`
- Purpose: Checks for sabotage building crate collisions
- Calls: None

### `isCarBombCrateCollide`
- Purpose: Checks for car bomb crate collisions
- Calls: None

### `isRailroad`
- Purpose: Identifies railroad collisions
- Calls: None

### `isSalvageCrateCollide`
- Purpose: Checks for salvage crate collisions
- Calls: None

## Globals
- None

## Dependencies
- `Common/Module.h`
-
