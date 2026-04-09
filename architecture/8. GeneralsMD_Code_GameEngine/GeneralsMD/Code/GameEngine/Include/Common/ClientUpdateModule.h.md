# GeneralsMD/Code/GameEngine/Include/Common/ClientUpdateModule.h

## Purpose
Defines the base class for client-side update modules in the SAGE engine.

## Responsibilities
- Declares the `ClientUpdateModule` abstract class
- Defines the interface for client-side updates
- Provides memory management macros for the class
- Specifies module type and interface mask constants

## Key Types
- `ClientUpdateModuleData` (Class): Module data type for client updates
- `ClientUpdateModule` (Class): Base class for client update modules
- `ClientUpdateModuleMagicEnum` (Enum): Not inferable (empty)
- `ClientUpdateModule_GLUE_NOT_IMPLEMENTED` (Enum): Not inferable (empty)

## Key Functions
### `ClientUpdateModule::clientUpdate`
- Purpose: Pure virtual function to be implemented by derived classes for client-side updates
- Calls: None

## Globals
- None

## Dependencies
- `Common/Module.h` (for `DrawableModule` and `ModuleData`)
- `stdlib.h` (standard library)
