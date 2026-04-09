# GeneralsMD/Code/GameEngine/Source/Common/RTS/MissionStats.cpp

## Purpose
Manages mission statistics tracking for units and buildings killed/lost per player.

## Responsibilities
- Initialize mission statistics
- Serialize/deserialize statistics via Xfer
- Provide CRC support for statistics
- Handle post-load processing

## Key Types
- MissionStats (Class): tracks mission statistics (units/buildings killed/lost per player)

## Key Functions
### MissionStats::MissionStats()
- Purpose: Constructor that initializes mission statistics
- Calls: init()

### MissionStats::init()
- Purpose: Resets all statistics counters to zero
- Calls: None

### MissionStats::crc()
- Purpose: Generates CRC checksum for mission statistics
- Calls: None

### MissionStats::xfer()
- Purpose: Serializes/deserializes mission statistics
- Calls: xferVersion(), xferUser(), xferInt()

### MissionStats::loadPostProcess()
- Purpose: Handles post-load processing (currently empty)
- Calls: None

## Globals
None

## Dependencies
- Common/MissionStats.h
- Common/Player.h
- Common/Xfer.h
- PreRTS.h
