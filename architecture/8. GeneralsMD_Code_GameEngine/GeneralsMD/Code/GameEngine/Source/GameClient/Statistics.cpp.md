# GeneralsMD/Code/GameEngine/Source/GameClient/Statistics.cpp

## Purpose
Provides statistical utility functions for normalization and Mu-law encoding.

## Responsibilities
- Implements Mu-law encoding for audio signal compression
- Provides range normalization functions
- Supports value remapping between different ranges

## Key Types
None

## Key Functions
### MuLaw
- Purpose: Encodes a value using Mu-law algorithm for compression
- Calls: `sign`, `log`, `fabs`

### Normalize
- Purpose: Normalizes a value to a 0-1 range
- Calls: None

### NormalizeToRange
- Purpose: Remaps a normalized value to a specified output range
- Calls: `Normalize`

## Globals
None

## Dependencies
- `PreRTS.h` (included first)
- `GameClient/Statistics.h` (header)
- `Real` type (floating-point)
- `sign` function (math utility)
