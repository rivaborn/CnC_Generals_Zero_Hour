# Generals/Code/GameEngine/Source/Common/Thing/DrawModule.cpp

## Purpose
This file contains the implementation of the `DrawModule` class, which is a base class for drawable modules in the game engine.

## Responsibilities
- Implements CRC and Xfer methods for data serialization.
- Extends base class functionality for loading post-processing.

## Key Types
- DrawModule (Class): Base class for drawable modules.

## Key Functions
### crc
- Purpose: Implements CRC method for data integrity checks.
- Calls: DrawableModule::crc

### xfer
- Purpose: Handles data transfer and versioning.
- Calls: XferVersion, DrawableModule::xfer

### loadPostProcess
- Purpose: Loads post-processing effects.
- Calls: DrawableModule::loadPostProcess

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/DrawModule.h"
  - "Common/Xfer.h"
