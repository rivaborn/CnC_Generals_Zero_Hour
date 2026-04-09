# GeneralsMD/Code/GameEngine/Source/Common/System/GameCommon.cpp

## Purpose
Provides utility functions and constants for game logic, including angle normalization and relationship/veterancy name lookups.

## Responsibilities
- Normalizes angles to the range [-Ï, Ï]
- Defines string constants for veterancy and relationship states
- Includes basic error handling for NaN values

## Key Types
None

## Key Functions
### normalizeAngle
- Purpose: Normalizes an angle to the range [-Ï, Ï]
- Calls: `_isnan` (from cmath)

## Globals
- TheVeterancyNames (const char*): Array of veterancy state strings
- TheRelationshipNames (const char*): Array of relationship state strings

## Dependencies
- `PreRTS.h` (included first)
- `Common/GameCommon.h` (header)
- `_isnan` (from cmath, used for NaN check)
