# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Destroy/DestroyModule.cpp

## Purpose
Base class implementation for the Destroy module in the game's behavior system.

## Responsibilities
- Provides foundational functionality for destruction-related behavior modules
- Manages serialization (Xfer) and CRC operations
- Handles post-load processing
- Serves as a base for derived destruction modules

## Key Types
- DestroyModule (Class): Base class for destruction behavior modules

## Key Functions
### DestroyModule::DestroyModule
- Purpose: Constructor for DestroyModule
- Calls: BehaviorModule constructor

### DestroyModule::~DestroyModule
- Purpose: Destructor for DestroyModule
- Calls: None

### DestroyModule::crc
- Purpose: Handles CRC calculation for serialization
- Calls: BehaviorModule::crc

### DestroyModule::xfer
- Purpose: Handles serialization/deserialization of module data
- Calls: BehaviorModule::xfer, XferVersion operations

### DestroyModule::loadPostProcess
- Purpose: Performs post-load initialization
- Calls: BehaviorModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Xfer.h
- GameLogic/Module/DestroyModule.h
- BehaviorModule (base class)
- Xfer (serialization class)
- XferVersion (version tracking)
