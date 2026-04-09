# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyCenterDockUpdate.h

## Purpose
Defines the SupplyCenterDockUpdate module, which converts cargo into money for the owning player.

## Responsibilities
- Converts cargo into money for the owning player
- Provides temporary stealth frames via module data
- Implements DockUpdate interface
- Handles module data parsing and management

## Key Types
- **SupplyCenterDockUpdateModuleData (Class)**: Holds module configuration including temporary stealth frames
- **SupplyCenterDockUpdate (Class)**: Main dock update class that processes cargo-to-money conversion
- **SupplyCenterDockUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **SupplyCenterDockUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### SupplyCenterDockUpdateModuleData::buildFieldParse
- Purpose: Parses INI field data for module configuration
- Calls: Not inferable

### SupplyCenterDockUpdate::action
- Purpose: Converts cargo into money for the owning player
- Calls: Not inferable

### SupplyCenterDockUpdate::update
- Purpose: Handles periodic update logic for the dock update
- Calls: Not inferable

## Globals
None

## Dependencies
- `Common/INI.h` (MultiIniFieldParse)
- `Common/GameMemory.h` (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- `GameLogic/Module/DockUpdate.h` (DockUpdate, DockUpdateModuleData, DockUpdateInterface)
