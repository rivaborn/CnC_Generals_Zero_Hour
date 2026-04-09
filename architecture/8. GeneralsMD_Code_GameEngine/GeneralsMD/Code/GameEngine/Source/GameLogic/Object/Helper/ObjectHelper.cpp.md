# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/ObjectHelper.cpp

## Purpose
Base class for object helper modules in the game logic system.

## Responsibilities
- Provides core functionality for object helpers
- Manages object sleep/wake cycles
- Handles serialization (Xfer) and CRC updates
- Serves as a base for derived helper modules

## Key Types
- ObjectHelper (Class): Base class for object helper modules

## Key Functions
### ~ObjectHelper
- Purpose: Virtual destructor for ObjectHelper.
- Calls: None

### sleepUntil
- Purpose: Puts the object to sleep until a specified frame.
- Calls: getObject(), getStatusBits(), test(), getFrame(), setWakeFrame()

### crc
- Purpose: Updates the module's CRC (Cyclic Redundancy Check).
- Calls: UpdateModule::crc()

### xfer
- Purpose: Serializes/deserializes the object helper's state.
- Calls: XferVersion, xferVersion(), UpdateModule::xfer()

### loadPostProcess
- Purpose: Handles post-processing after loading.
- Calls: UpdateModule::loadPostProcess()

## Globals
- None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/Module/ObjectHelper.h
- Xfer, Object, UpdateModule, TheGameLogic (external symbols)
