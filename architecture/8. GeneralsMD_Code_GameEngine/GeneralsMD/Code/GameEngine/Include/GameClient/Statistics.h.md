# GeneralsMD/Code/GameEngine/Include/GameClient/Statistics.h

## Purpose
Header file defining utility functions for statistical calculations and value normalization.

## Responsibilities
- Declares mathematical utility functions for value transformation
- Provides Mu-Law companding function for audio-like scaling
- Offers range normalization functions for value mapping

## Key Types
None

## Key Functions
### MuLaw
- Purpose: Applies Mu-Law companding to a value for non-linear scaling
- Calls: Not inferable

### Normalize
- Purpose: Maps a value from an input range to [0, 1]
- Calls: Not inferable

### NormalizeToRange
- Purpose: Maps a value from an input range to a specified output range
- Calls: Not inferable

## Globals
None

## Dependencies
- `Lib/Basetype.h` (for `Real` type definition)
- Uses `Real` type (floating-point number)
