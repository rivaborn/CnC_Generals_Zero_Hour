# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StickyBombUpdate.h

## Purpose
Defines the StickyBombUpdate module for attaching and updating sticky bombs on objects in the game.

## Responsibilities
- Manages sticky bomb attachment to target objects
- Handles bomb detonation logic
- Updates bomb position based on target bone
- Provides timed bomb functionality

## Key Types
- **StickyBombUpdateModuleData (Class)**: Contains configuration data for the sticky bomb (bone attachment, offset, damage weapon, FX)
- **StickyBombUpdate (Class)**: Main module class handling bomb behavior and updates
- **WeaponTemplate (Class)**: Reference to damage weapon template (external)
- **FXList (Class)**: Reference to explosion effects (external)

## Key Functions
### StickyBombUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data
- Calls: UpdateModuleData::buildFieldParse

### StickyBombUpdate::update
- Purpose: Updates bomb position each frame
- Calls: Not inferable (implementation in .cpp)

### StickyBombUpdate::detonate
- Purpose: Triggers bomb explosion
- Calls: Not inferable

### StickyBombUpdate::initStickyBomb
- Purpose: Initializes bomb attachment to target
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- WeaponTemplate (forward declaration)
- FXList (forward declaration)
- INI parsing utilities (INI namespace)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macro (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
