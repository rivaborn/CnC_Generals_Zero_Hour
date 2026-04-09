# Generals/Code/GameEngine/Source/Common/RTS/MissionStats.cpp

## Purpose
This file contains the implementation for the `MissionStats` class, which manages statistics related to a mission in Command & Conquer Generals.

## Responsibilities
- Initializes and tracks units and buildings killed and lost.
- Implements CRC (Cyclic Redundancy Check) and Xfer methods for data transfer.
- Handles post-load processing.

## Key Types
- `MissionStats` (Class): Manages mission statistics.

## Key Functions
### MissionStats::init
- Purpose: Initializes the mission statistics by setting counts of units and buildings killed and lost to zero.
- Calls: None

### MissionStats::crc
- Purpose: Implements CRC method for data integrity checks.
- Calls: None

### MissionStats::xfer
- Purpose: Handles data transfer for mission statistics, including versioning and specific data fields.
- Calls: `Xfer::xferVersion`, `Xfer::xferUser`, `Xfer::xferInt`

### MissionStats::loadPostProcess
- Purpose: Performs post-load processing after mission statistics are loaded.
- Calls: None

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/MissionStats.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
