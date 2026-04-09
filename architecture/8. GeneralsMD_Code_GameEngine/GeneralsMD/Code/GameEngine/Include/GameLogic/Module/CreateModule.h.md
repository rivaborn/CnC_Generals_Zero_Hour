# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CreateModule.h

## Purpose
Defines the base class and interface for object creation modules in the game logic system.

## Responsibilities
- Declares `CreateModuleInterface` for creation lifecycle callbacks
- Provides `CreateModule` base class implementing the interface
- Manages creation and build completion events for game objects
- Handles memory pooling and module serialization macros

## Key Types
- **CreateModuleInterface (Class)**: Abstract interface for creation lifecycle callbacks
- **CreateModuleData (Class)**: Data container for creation module (inherits from `BehaviorModuleData`)
- **CreateModule (Class)**: Concrete base class implementing creation module behavior
- **CreateModuleMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **CreateModule_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### CreateModule::onCreate
- Purpose: Pure virtual function called when object becomes a code object
- Calls: None

### CreateModule::onBuildComplete
- Purpose: Virtual function called when object is fully constructed
- Calls: None

### CreateModule::shouldDoOnBuildComplete
- Purpose: Checks if onBuildComplete should be called
- Calls: None

## Globals
- None

## Dependencies
- `Common/Module.h`
- `GameLogic/Module/BehaviorModule.h`
- `MultiIniFieldParse` (used in `buildFieldParse`)
- `Thing` class (used in constructor)
- `ModuleData` class
- Memory pool and module macro systems (internal)
