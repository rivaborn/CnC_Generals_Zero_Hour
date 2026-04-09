# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyWarehouseDockUpdate.h

## Purpose
Defines the SupplyWarehouseDockUpdate module for handling supply box transfers during docking actions in the game.

## Responsibilities
- Manages supply box transfers between docked objects
- Handles dock cripple state and its effects
- Provides interface for querying stored boxes
- Configures initial supply box count and deletion behavior

## Key Types
- **SupplyWarehouseDockUpdateModuleData (Class)**: Stores module configuration data (starting boxes, deletion flag)
- **SupplyWarehouseDockUpdate (Class)**: Implements the docking update logic for supply warehouses
- **SupplyWarehouseDockUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **SupplyWarehouseDockUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### `SupplyWarehouseDockUpdate::action`
- Purpose: Handles supply box transfers during docking
- Calls: Not visible in header

### `SupplyWarehouseDockUpdate::setDockCrippled`
- Purpose: Configures dock operational state
- Calls: Not visible in header

### `SupplyWarehouseDockUpdate::onObjectCreated`
- Purpose: Initialization when object is created
- Calls: Not visible in header

## Globals
- None

## Dependencies
- `Common/INI.h` (for configuration parsing)
- `Common/GameMemory.h` (for memory management macros)
- `GameLogic/Module/DockUpdate.h` (base class)
- `DockUpdateModuleData` (base class for module data)
- `DockUpdateInterface` (interface type)
- `Thing`, `Object` (game entity types)
