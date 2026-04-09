# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/CreateModule.cpp

## Purpose
Base class implementation for the Create module in the game's behavior system.

## Responsibilities
- Provides core functionality for object creation behavior
- Manages serialization (Xfer) and CRC operations
- Handles post-load processing
- Maintains a flag for build completion handling

## Key Types
- CreateModule (Class): Base class for creation behavior modules

## Key Functions
### CreateModule::CreateModule
- Purpose: Constructor initializes the module with a Thing and ModuleData
- Calls: BehaviorModule constructor

### CreateModule::~CreateModule
- Purpose: Destructor (empty implementation)
- Calls: None

### CreateModule::crc
- Purpose: Handles CRC calculation for serialization
- Calls: BehaviorModule::crc

### CreateModule::xfer
- Purpose: Serialization method with versioning support
- Calls: BehaviorModule::xfer, XferVersion, XferBool

### CreateModule::loadPostProcess
- Purpose: Post-load processing hook
- Calls: BehaviorModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Xfer.h
- GameLogic/Module/CreateModule.h
- BehaviorModule (base class)
- Xfer (serialization class)
- Thing (game object class)
- ModuleData (module configuration data)
