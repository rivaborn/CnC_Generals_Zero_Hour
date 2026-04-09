# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/colmath.h

## Purpose
Header file defining collision detection math utilities for the SAGE engine.

## Responsibilities
- Declares geometric primitives (planes, boxes, spheres, etc.)
- Provides intersection and overlap testing functions
- Supports collision queries with movement vectors
- Includes statistical tracking for collision tests

## Key Types
- **AAPlaneClass (Class)**: Axis-aligned plane
- **PlaneClass (Class)**: General plane
- **LineSegClass (Class)**: Line segment
- **TriClass (Class)**: Triangle
- **SphereClass (Class)**: Sphere
- **AABoxClass (Class)**: Axis-aligned bounding box
- **OBBoxClass (Class)**: Oriented bounding box
- **FrustumClass (Class)**: View frustum
- **OverlapType (Enum)**: Classification of spatial relationships (POS/NEG/ON/BOTH)
- **ColmathStatsStruct (Class)**: Statistics tracking for collision tests

## Key Functions
### Intersection_Test
- Purpose: Tests if two geometric objects intersect
- Calls: None (pure declarations)

### Overlap_Test
- Purpose: Classifies spatial relationship between objects
- Calls: eval_overlap_mask, eval_overlap_collision

### Collide
- Purpose: Tests collision with movement vectors
- Calls: None (pure declarations)

### eval_overlap_mask
- Purpose: Converts vertex mask to OverlapType
- Calls: None

### eval_overlap_collision
- Purpose: Determines overlap from CastResultStruct
- Calls: None

## Globals
- **COLLISION_EPSILON (float)**: Precision threshold for collision tests
- **Stats (ColmathStatsStruct)**: Global statistics tracker

## Dependencies
- "always.h", "vector3.h", "castres.h"
- CastResultStruct (external)
- Forward declarations of geometric classes
