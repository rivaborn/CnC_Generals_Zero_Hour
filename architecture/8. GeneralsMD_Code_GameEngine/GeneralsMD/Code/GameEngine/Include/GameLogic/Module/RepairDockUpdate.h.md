# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RepairDockUpdate.h

## Purpose
Defines the repair dock update module for vehicle repair functionality in the game.

## Responsibilities
- Manages repair dock behavior for vehicles
- Handles health restoration over time
- Provides docking interface for repair actions
- Tracks repair progress between frames

## Key Types
- **RepairDockUpdateModuleData (Class)**: Contains repair timing parameters
- **RepairDockUpdate (Class)**: Implements repair dock logic
- **RepairDockUpdateMagicEnum (Enum)**: Not inferable
- **RepairDockUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### RepairDockUpdateModuleData::buildFieldParse
- Purpose: Parses configuration data for repair dock settings
- Calls: Not inferable

### RepairDockUpdate::action
- Purpose: Performs the repair action on docked objects
- Calls: Not inferable

### RepairDockUpdate::isRallyPointAfterDockType
- Purpose: Determines if rally point command should be issued after docking
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/GameMemory.h`
- `GameLogic/Module/SupplyCenterDockUpdate.h`
- Inherits from `DockUpdateModuleData` and `DockUpdate`
