# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmath.cpp

## Purpose
Implements collision detection statistics tracking for the CollisionMath class.

## Responsibilities
- Defines collision detection statistics structure
- Initializes and resets collision statistics
- Tracks various collision test types (ray-tri, box-tri, box-box)

## Key Types
- ColmathStatsStruct (struct): Holds counters for different collision test types and results

## Key Functions
### ColmathStatsStruct::ColmathStatsStruct
- Purpose: Constructor that initializes the statistics structure
- Calls: Reset()

### ColmathStatsStruct::Reset
- Purpose: Resets all collision statistics counters to zero
- Calls: None

## Globals
- COINCIDENCE_EPSILON (float): Small value used for floating-point comparisons in collision detection
- Stats (ColmathStatsStruct): Global instance tracking collision statistics

## Dependencies
- "colmath.h" header file
- CollisionMath class (external)
