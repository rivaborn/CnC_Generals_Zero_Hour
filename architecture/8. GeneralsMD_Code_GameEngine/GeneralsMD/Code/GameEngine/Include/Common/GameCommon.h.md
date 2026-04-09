# GeneralsMD/Code/GameEngine/Include/Common/GameCommon.h

## Purpose
Header file containing common game types, enums, and utility functions used across the game engine.

## Responsibilities
- Defines core game enums (difficulty, player types, shroud states, etc.)
- Provides time/velocity conversion utilities
- Implements doubly-linked list (DLINK) template and macros
- Declares relationship and veterancy systems

## Key Types
- `PlayerMaskType` (Type): Bitmask for player identification
- `GameDifficulty` (Enum): Game difficulty levels
- `PlayerType` (Enum): Human/computer player classification
- `CellShroudStatus` (Enum): Map cell visibility states
- `ObjectShroudStatus` (Enum): Object visibility states
- `VeterancyLevel` (Enum): Unit experience levels
- `CommandSourceType` (Enum): Command origin types
- `AbleToAttackType` (Enum): Attack capability flags
- `WhichTurretType` (Enum): Turret identification
- `Relationship` (Enum): Player relationship types
- `DLINK_ITERATOR` (Class): Doubly-linked list iterator template

## Key Functions
### `ConvertDurationFromMsecsToFrames`
- Purpose: Convert milliseconds to game logic frames
- Calls: None

### `ConvertVelocityInSecsToFrames`
- Purpose: Convert velocity from m/s to frames
- Calls: None

### `ConvertAccelerationInSecsToFrames`
- Purpose: Convert acceleration from m/sÂ² to frames
- Calls: None

### `ConvertAngularVelocityInDegreesPerSecToRadsPerFrame`
- Purpose: Convert angular velocity to radians per frame
- Calls: None

### `isForcedAttack`
- Purpose: Check if attack is forced
- Calls: None

### `isContinuedAttack`
- Purpose: Check if attack is continued
- Calls: None

### `normalizeAngle`
- Purpose: Normalize angle to -Ï...Ï range
- Calls: None

### `stdAngleDiff`
- Purpose: Calculate normalized angle difference
- Calls: `normalizeAngle`

## Globals
- `LOGICFRAMES_PER_MSEC_REAL` (Real): Frames per millisecond constant
- `MSEC_PER_LOGICFRAME_REAL` (Real): Milliseconds per frame constant
- `LOGICFRAMES_PER_SECONDS_REAL` (Real): Frames per second constant
- `SECONDS_PER_LOGICFRAME_REAL` (Real): Seconds per frame constant
- `PLAYERMASK_ALL` (PlayerMaskType): Bitmask for all players
- `PLAYERMASK_NONE` (PlayerMaskType): Bitmask for no players
- `TheVeterancyNames` (const char*): Veterancy level names array
- `VETERANCY_LEVEL_FLAGS_ALL` (VeterancyLevelFlags): All veterancy flags
- `VETERANCY_LEVEL_FLAGS_NONE` (VeterancyLevelFlags): No veterancy flags
- `TheRelationshipNames` (const char*): Relationship names array

## Dependencies
- `Lib/BaseType.h` (include)
- `Real`, `Bool`, `UnsignedShort`, `UnsignedInt` (types)
- `PI` (constant)
