# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BehaviorModule.cpp

## Purpose
Implements base functionality for the BehaviorModule class, handling serialization and post-load processing.

## Responsibilities
- Serialization/deserialization via Xfer
- CRC (checksum) generation
- Post-load initialization
- Inherits from ObjectModule

## Key Types
- None (only implements BehaviorModule methods)

## Key Functions
### BehaviorModule::crc
- Purpose: Generates CRC checksum for the module.
- Calls: ObjectModule::crc

### BehaviorModule::xfer
- Purpose: Handles serialization/deserialization of the module.
- Calls: ObjectModule::xfer, Xfer::xferVersion

### BehaviorModule::loadPostProcess
- Purpose: Performs post-load initialization.
- Calls: ObjectModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Xfer.h
- GameLogic/Module/BehaviorModule.h
- ObjectModule (base class)
