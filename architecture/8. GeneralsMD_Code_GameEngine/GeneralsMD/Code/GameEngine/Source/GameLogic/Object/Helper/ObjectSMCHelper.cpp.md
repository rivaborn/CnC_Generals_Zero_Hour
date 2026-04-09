# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/ObjectSMCHelper.cpp

## Purpose
Handles Special Model Condition (SMC) states for game objects, clearing them when triggered.

## Responsibilities
- Clears SMC states on object
- Implements update loop for SMC handling
- Provides serialization (Xfer) and CRC support
- Handles post-load processing

## Key Types
- None

## Key Functions
### `~ObjectSMCHelper`
- Purpose: Destructor for ObjectSMCHelper.
- Calls: None

### `update`
- Purpose: Clears SMC states and returns sleep forever.
- Calls: `getObject()->clearSpecialModelConditionStates()`

### `crc`
- Purpose: Serializes/deserializes CRC data.
- Calls: `ObjectHelper::crc()`

### `xfer`
- Purpose: Handles object serialization/deserialization.
- Calls: `ObjectHelper::xfer()`

### `loadPostProcess`
- Purpose: Post-load processing for the helper.
- Calls: `ObjectHelper::loadPostProcess()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/ObjectSMCHelper.h`
- `Xfer`, `ObjectHelper`, `UpdateSleepTime`
