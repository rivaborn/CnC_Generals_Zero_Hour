# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectRepulsorHelper.h

## Purpose
Defines the ObjectRepulsorHelper class, a module for handling object repulsion logic in the game.

## Responsibilities
- Inherits from ObjectHelper to provide repulsion behavior
- Manages update logic for repulsor effects
- Uses memory pool allocation for performance
- Provides standard module macros for game engine integration

## Key Types
- **ObjectRepulsorHelperModuleData (Class)**: Module data container (empty implementation)
- **ObjectRepulsorHelper (Class)**: Main helper class for repulsion logic
- **ObjectRepulsorHelperMagicEnum (Enum)**: Not inferable (likely unused)
- **ObjectRepulsorHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused)

## Key Functions
### ObjectRepulsorHelper::update
- Purpose: Handles periodic repulsion updates
- Calls: Not inferable (implementation in .cpp file)

## Globals
- None

## Dependencies
- "GameLogic/Module/ObjectHelper.h" (base class)
- MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA (module system macros)
- MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE (memory management macros)
