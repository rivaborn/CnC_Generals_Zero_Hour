# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/BodyModule.cpp

## Purpose
Implements the `BodyModule` class, a base class for behavior modules handling physical body attributes in the game.

## Responsibilities
- Serialization/deserialization via `Xfer` system
- CRC (checksum) generation
- Post-load processing
- Damage scalar management

## Key Types
- `BodyModule` (Class): Base class for body-related behavior modules
- `BehaviorModule` (Class): Parent class (not defined here)

## Key Functions
### `crc`
- Purpose: Generates a checksum for the module.
- Calls: `BehaviorModule::crc`

### `xfer`
- Purpose: Serializes/deserializes the module's state.
- Calls: `BehaviorModule::xfer`, `xfer->xferVersion`, `xfer->xferReal`

### `loadPostProcess`
- Purpose: Handles post-load initialization.
- Calls: `BehaviorModule::loadPostProcess`

## Globals
- `m_damageScalar` (Real): Damage multiplier for the body (not shown in header, inferred from `xfer`)

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Module/BodyModule.h`
- `Xfer` class, `BehaviorModule` class
