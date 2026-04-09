# GeneralsMD/Code/GameEngine/Include/Common/AudioRandomValue.h

## Purpose
Provides random number generation utilities for audio-related operations in the game.

## Responsibilities
- Declares functions for generating random integers and real numbers.
- Defines macros for simplified access to random value functions.
- Ensures random values are tracked with file/line information for debugging.

## Key Types
None

## Key Functions
### GetGameAudioRandomValue
- Purpose: Generates a random integer between `lo` and `hi`.
- Calls: None (external implementation)

### GetGameAudioRandomValueReal
- Purpose: Generates a random real number between `lo` and `hi`.
- Calls: None (external implementation)

## Globals
None

## Dependencies
- `Lib/BaseType.h` (for `Int` and `Real` types)
- `__FILE__` and `__LINE__` (preprocessor macros)
