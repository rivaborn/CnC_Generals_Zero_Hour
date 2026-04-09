# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DestroyModule.h

## Purpose
Defines the DestroyModule interface and implementation for handling object destruction in the game engine.

## Responsibilities
- Provides a base interface for destruction behavior
- Implements a BehaviorModule subclass for destruction logic
- Defines memory management macros for the module
- Exposes destruction interface via getDestroy()

## Key Types
- DestroyModuleInterface (Class): abstract interface for destruction callbacks
- DestroyModule (Class): concrete BehaviorModule implementing destruction logic
- DestroyModuleMagicEnum (Enum): Not inferable (likely macro-related)
- DestroyModule_GLUE_NOT_IMPLEMENTED (Enum): Not inferable (likely macro-related)

## Key Functions
### DestroyModule::DestroyModule
- Purpose: Constructor for DestroyModule
- Calls: Not inferable (constructor body not shown)

### DestroyModule::getInterfaceMask
- Purpose: Returns the module's interface mask
- Calls: None

### DestroyModule::getDestroy
- Purpose: Returns the destruction interface
- Calls: None

### DestroyModule::onDestroy
- Purpose: Pure virtual function for destruction handling
- Calls: None

## Globals
None

## Dependencies
- Common/Module.h
- GameLogic/Module/BehaviorModule.h
- MODULEINTERFACE_DESTROY constant
- MEMORY_POOL_GLUE_ABC macro
- MAKE_STANDARD_MODULE_MACRO_ABC macro
