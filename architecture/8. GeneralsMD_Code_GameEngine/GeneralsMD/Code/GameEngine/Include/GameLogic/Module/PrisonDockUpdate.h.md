# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PrisonDockUpdate.h

## Purpose
Header file defining the PrisonDockUpdate class, which handles docking updates for prison structures in the game.

## Responsibilities
- Inherits from DockUpdate to provide prison-specific docking behavior
- Implements the action() method to perform prison-related operations
- Manages memory allocation via MEMORY_POOL_GLUE macro
- Provides DockUpdateInterface access via getDockUpdateInterface()
- Conditionally compiled only when ALLOW_SURRENDER is defined

## Key Types
- PrisonDockUpdate (Class): Extends DockUpdate to handle prison structure docking logic

## Key Functions
### PrisonDockUpdate(Thing *thing, const ModuleData* moduleData)
- Purpose: Constructor for PrisonDockUpdate
- Calls: Not inferable (constructor implementation not shown)

### getDockUpdateInterface()
- Purpose: Returns the DockUpdateInterface for this object
- Calls: None

### action(Object *docker, Object *drone = NULL)
- Purpose: Executes prison-specific docking actions
- Calls: Not inferable (implementation not shown)

## Globals
None

## Dependencies
- Common/GameMemory.h: For memory pool macros
- GameLogic/Module/DockUpdate.h: Base class definition
- ALLOW_SURRENDER: Compile-time conditional flag
