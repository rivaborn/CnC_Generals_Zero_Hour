# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectSMCHelper.h

## Purpose
Defines the ObjectSMCHelper class, a module for handling SMC (State Machine Controller) related logic for game objects.

## Responsibilities
- Inherits from ObjectHelper to extend object behavior
- Manages SMC-specific updates for game objects
- Provides memory pool management for instances
- Implements standard module macros for registration

## Key Types
- **ObjectSMCHelperModuleData (Class)**: Module data container for ObjectSMCHelper
- **ObjectSMCHelper (Class)**: Main helper class for SMC object logic
- **ObjectSMCHelperMagicEnum (Enum)**: Not inferable (empty definition)
- **ObjectSMCHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty definition)

## Key Functions
### update
- Purpose: Handles periodic updates for SMC-controlled objects
- Calls: Not inferable (implementation not shown)

## Globals
- None

## Dependencies
- **ObjectHelper.h**: Base class for object helpers
- **ModuleData**: Base class for module data
- **Thing**: Game object base class
- **Memory pool macros**: For object instantiation management
