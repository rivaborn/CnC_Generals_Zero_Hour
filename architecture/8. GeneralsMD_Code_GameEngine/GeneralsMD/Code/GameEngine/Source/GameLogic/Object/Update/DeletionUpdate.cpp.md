# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DeletionUpdate.cpp

## Purpose
Handles object deletion after a random lifetime delay.

## Responsibilities
- Manages object lifetime via frame countdown
- Destroys object when lifetime expires
- Supports serialization and CRC for networking

## Key Types
- `DeletionUpdate` (Class): Update module that deletes its parent object after a delay

## Key Functions
### `DeletionUpdate::DeletionUpdate`
- Purpose: Initializes deletion timer with random delay
- Calls: `calcSleepDelay`, `setWakeFrame`

### `DeletionUpdate::update`
- Purpose: Destroys object when lifetime expires
- Calls: `TheGameLogic->destroyObject`

### `DeletionUpdate::calcSleepDelay`
- Purpose: Computes random delay between min/max frames
- Calls: `GameLogicRandomValue`

### `DeletionUpdate::xfer`
- Purpose: Serializes module state for networking
- Calls: `UpdateModule::xfer`

## Globals
- None

## Dependencies
- `UpdateModule`, `Thing`, `DeletionUpdateModuleData`, `Xfer`, `TheGameLogic`
