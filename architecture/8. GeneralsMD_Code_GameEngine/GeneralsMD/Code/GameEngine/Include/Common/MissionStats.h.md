# GeneralsMD/Code/GameEngine/Include/Common/MissionStats.h

## Purpose
Defines the `MissionStats` class for tracking mission-related statistics during gameplay.

## Responsibilities
- Tracks units and buildings killed/lost per player
- Provides snapshot serialization for network sync
- Supports scoring and AI decision-making

## Key Types
- **MissionStats (Class)**: Tracks mission statistics (units/structures killed/lost per player).

## Key Functions
### MissionStats()
- Purpose: Default constructor.
- Calls: None.

### init()
- Purpose: Resets all statistics to zero.
- Calls: None.

### crc(Xfer *xfer)
- Purpose: Computes CRC for snapshot serialization.
- Calls: None.

### xfer(Xfer *xfer)
- Purpose: Serializes/deserializes mission stats.
- Calls: None.

### loadPostProcess()
- Purpose: Post-processing after loading snapshot data.
- Calls: None.

## Globals
- None.

## Dependencies
- `Lib/BaseType.h` (Int)
- `Common/GameCommon.h` (MAX_PLAYER_COUNT)
- `Common/Snapshot.h` (Snapshot, Xfer)
