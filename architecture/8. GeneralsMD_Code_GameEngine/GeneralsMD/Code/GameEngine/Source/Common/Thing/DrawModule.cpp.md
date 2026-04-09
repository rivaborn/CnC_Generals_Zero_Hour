# GeneralsMD/Code/GameEngine/Source/Common/Thing/DrawModule.cpp

## Purpose
Implements the base class for draw modules in the SAGE engine, handling serialization and post-processing.

## Responsibilities
- Provides CRC (checksum) functionality for the module
- Implements Xfer (serialization) logic
- Handles post-load processing
- Extends DrawableModule base class

## Key Types
- None

## Key Functions
### `crc`
- Purpose: Generates a checksum for the module.
- Calls: `DrawableModule::crc`

### `xfer`
- Purpose: Serializes/deserializes the module state.
- Calls: `Xfer::xferVersion`, `DrawableModule::xfer`

### `loadPostProcess`
- Purpose: Executes post-load processing.
- Calls: `DrawableModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`
- `Common/DrawModule.h`
- `Common/Xfer.h`
- `DrawableModule` (base class)
- `Xfer` (external class)
