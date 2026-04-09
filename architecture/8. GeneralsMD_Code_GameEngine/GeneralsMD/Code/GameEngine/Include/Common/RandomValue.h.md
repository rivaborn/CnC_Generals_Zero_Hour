# GeneralsMD/Code/GameEngine/Include/Common/RandomValue.h

## Purpose
Header for random number generation utilities used in game logic and replay systems.

## Responsibilities
- Declares random number initialization functions
- Provides access to game logic random seed for replays
- Exposes seed CRC calculation for checksums

## Key Types
None

## Key Functions
### InitRandom
- Purpose: Initialize random number generator with default or specified seed
- Calls: Not inferable

### InitGameLogicRandom
- Purpose: Initialize game logic random seed to known value at game start
- Calls: Not inferable

### GetGameLogicRandomSeed
- Purpose: Retrieve current game logic random seed for replay purposes
- Calls: Not inferable

### GetGameLogicRandomSeedCRC
- Purpose: Calculate CRC of game logic random seed for checksum verification
- Calls: Not inferable

## Globals
None

## Dependencies
- `Lib/BaseType.h` (for `UnsignedInt` type)
- External random number generation implementation (not defined here)
