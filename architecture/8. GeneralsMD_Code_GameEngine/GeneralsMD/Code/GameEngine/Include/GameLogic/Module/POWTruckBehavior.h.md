# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/POWTruckBehavior.h

## Purpose
Defines behavior for POW trucks in the game, handling collision logic when the truck interacts with other objects.

## Responsibilities
- Manages POW truck module data and behavior
- Handles collision events for POW trucks
- Extends OpenContain functionality for POW-specific behavior
- Provides field parsing for module configuration

## Key Types
- POWTruckBehaviorModuleData (Class): Module data for POW truck behavior, extends OpenContainModuleData
- POWTruckBehavior (Class): Main behavior class for POW trucks, extends OpenContain

## Key Functions
### POWTruckBehavior::onCollide
- Purpose: Handles collision events for POW trucks
- Calls: Not inferable (implementation in .cpp file)

## Globals
- None

## Dependencies
- GameLogic/Module/OpenContain.h
- MultiIniFieldParse (external)
- Thing, Object, Coord3D (external)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
