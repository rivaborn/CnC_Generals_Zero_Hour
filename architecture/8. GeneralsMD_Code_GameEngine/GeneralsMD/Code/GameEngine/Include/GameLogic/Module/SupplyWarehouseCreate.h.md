# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyWarehouseCreate.h

## Purpose
Handles logic when a Supply Warehouse is created, updating resource management for all players.

## Responsibilities
- Manages Supply Warehouse creation events
- Updates resource brains for all players
- Inherits from CreateModule for module functionality

## Key Types
- **SupplyWarehouseCreate (Class)**: Module for Supply Warehouse creation logic
- **SupplyWarehouseCreateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **SupplyWarehouseCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### SupplyWarehouseCreate()
- Purpose: Constructor for SupplyWarehouseCreate module
- Calls: Not inferable (constructor body not shown)

### onCreate()
- Purpose: Handles logic when Supply Warehouse is created
- Calls: Not inferable (implementation not shown)

## Globals
- None

## Dependencies
- `CreateModule.h` (base class)
- `Thing` class (forward-declared)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macros (`MAKE_STANDARD_MODULE_MACRO`)
