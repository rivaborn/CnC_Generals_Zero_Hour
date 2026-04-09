# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/ObjectRepulsorHelper.cpp

## Purpose
Handles repulsor behavior for game objects, managing status and updates.

## Responsibilities
- Clears repulsor status on update
- Manages object helper lifecycle (destruction, serialization, loading)
- Provides base class overrides for Xfer and CRC operations

## Key Types
- `ObjectRepulsorHelper` (Class): Manages repulsor behavior for game objects

## Key Functions
### `~ObjectRepulsorHelper`
- Purpose: Destructor for the repulsor helper
- Calls: None

### `update`
- Purpose: Clears repulsor status and returns sleep forever
- Calls: `getObject()->clearStatus`

### `crc`
- Purpose: Serialization CRC for the helper
- Calls: `ObjectHelper::crc`

### `xfer`
- Purpose: Serialization method for the helper
- Calls: `ObjectHelper::xfer`, `xfer->xferVersion`

### `loadPostProcess`
- Purpose: Post-load processing for the helper
- Calls: `ObjectHelper::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/ObjectRepulsorHelper.h`
- `ObjectHelper`, `Xfer`, `Object`, `UpdateSleepTime`, `XferVersion`
