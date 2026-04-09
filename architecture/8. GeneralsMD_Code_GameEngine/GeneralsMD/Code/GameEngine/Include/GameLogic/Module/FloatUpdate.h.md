# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FloatUpdate.h

## Purpose
Defines a game module for handling floating-on-water behavior for game objects.

## Responsibilities
- Manages floating update logic for objects
- Provides module data configuration
- Handles enable/disable state for floating
- Implements update timing for floating behavior

## Key Types
- **FloatUpdateModuleData (Class)**: Module data configuration for floating behavior
- **FloatUpdate (Class)**: Main floating update module class
- **FloatUpdateMagicEnum (Enum)**: Not inferable
- **FloatUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### FloatUpdate::update
- Purpose: Determines whether to perform floating updates
- Calls: Not inferable

### FloatUpdate::setEnabled
- Purpose: Enables or disables floating behavior
- Calls: None

## Globals
- None

## Dependencies
- UpdateModule.h
- FieldParse struct (forward reference)
- MultiIniFieldParse class
- Thing class
- ModuleData class
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Standard module macros (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
