# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/LifetimeUpdate.cpp

## Purpose
Manages object lifetime by counting down frames and destroying the object when the count reaches zero.

## Responsibilities
- Initializes lifetime based on min/max frame range
- Handles special case for Hulk objects with override lifetime
- Calculates random sleep delay for lifetime
- Kills object when lifetime expires
- Serializes/deserializes lifetime data

## Key Types
- **LifetimeUpdate (Class)**: Manages object lifetime expiration
- **LifetimeUpdateModuleData (Struct)**: Not inferable (used in base class)

## Key Functions
### LifetimeUpdate()
- Purpose: Constructor initializes lifetime based on module data
- Calls: calcSleepDelay(), getLifetimeUpdateModuleData(), setWakeFrame()

### setLifetimeRange()
- Purpose: Sets new lifetime range and updates wake frame
- Calls: calcSleepDelay(), setWakeFrame()

### calcSleepDelay()
- Purpose: Calculates random delay between min/max frames
- Calls: GameLogicRandomValue()

### update()
- Purpose: Kills object when lifetime expires
- Calls: getObject()->kill()

### xfer()
- Purpose: Serializes/deserializes lifetime data
- Calls: UpdateModule::xfer(), xfer->xferVersion(), xfer->xferUnsignedInt()

## Globals
- **TheGameLogic (GameLogic**)**: Global game logic instance

## Dependencies
- PreRTS.h, Common/RandomValue.h, Common/Xfer.h, GameLogic/GameLogic.h, GameLogic/Module/LifetimeUpdate.h, GameLogic/Object.h
- UpdateModule (base class), Thing (base class), Xfer (serialization)
