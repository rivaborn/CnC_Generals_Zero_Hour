# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DynamicGeometryInfoUpdate.h

## Purpose
Defines a module for dynamically updating an object's geometry properties over time.

## Responsibilities
- Manages smooth transitions between initial and final geometry parameters
- Handles timing and direction of geometry updates
- Provides module data configuration for initialization
- Implements update logic for geometry interpolation

## Key Types
- **DynamicGeometryInfoUpdateModuleData (Class)**: Stores configuration parameters for geometry transitions
- **DynamicGeometryInfoUpdate (Class)**: Implements the update module that modifies object geometry
- **DynamicGeometryDirection (Enum)**: Defines direction constants (FORWARD, BACKWARD)

## Key Functions
### DynamicGeometryInfoUpdate::update
- Purpose: Updates the object's geometry based on elapsed time and configuration
- Calls: Not inferable (implementation in .cpp file)

### DynamicGeometryInfoUpdateModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable (implementation in .cpp file)

## Globals
- None

## Dependencies
- `Common/Geometry.h`
- `GameLogic/Module/UpdateModule.h`
- `ModuleData` class
- `MultiIniFieldParse` class
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Standard module macros (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
