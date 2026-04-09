# Generals/Code/Libraries/Source/WWVegas/WWMath/colmath.cpp

## Purpose
Implements collision detection math utilities and statistics tracking for the game engine.

## Responsibilities
- Defines collision math constants and statistics structures
- Initializes and resets collision statistics counters
- Provides foundation for collision detection calculations

## Key Types
- CollisionMath::ColmathStatsStruct (struct): Tracks various collision detection statistics

## Key Functions
### CollisionMath::ColmathStatsStruct::ColmathStatsStruct
- Purpose: Constructor that initializes collision statistics
- Calls: Reset()

### CollisionMath::ColmathStatsStruct::Reset
- Purpose: Resets all collision statistics counters to zero
- Calls: None

## Globals
- CollisionMath::COINCIDENCE_EPSILON (const float): Small value used for floating-point comparisons
- CollisionMath::Stats (ColmathStatsStruct): Global statistics tracker instance

## Dependencies
- "colmath.h" header
- Uses float type from standard library
