# Generals/Code/Libraries/Source/WWVegas/WWMath/colmath.h

## Purpose
Header file defining collision detection math utilities for the SAGE engine.

## Responsibilities
- Declares geometric primitives (planes, boxes, spheres, etc.)
- Provides intersection/overlap/collision test functions
- Defines statistics tracking for collision math
- Exposes epsilon constants for collision precision

## Key Types
- **AAPlaneClass (Class)**: Axis-aligned plane
- **PlaneClass (Class)**: General plane
- **LineSegClass (Class)**: Line segment
- **TriClass (Class)**: Triangle
- **SphereClass (Class)**: Sphere
- **AABoxClass (Class)**: Axis-aligned bounding box
- **OBBoxClass (Class)**: Oriented bounding box
- **FrustumClass (Class)**: View frustum
- **CollisionMath (Class)**: Collision detection utility class
- **OverlapType (Enum)**: Result of overlap tests (POS/NEG/ON/BOTH)
- **ColmathStatsStruct (Class)**: Statistics tracking structure

## Key Functions
### Intersection_Test
- Purpose: Test if two geometric objects intersect
- Calls: None (pure declarations)

### Overlap_Test
- Purpose: Classify object B relative to object A
- Calls: eval_overlap_mask, eval_overlap_collision

### Collide
- Purpose: Test collision between moving objects
- Calls: None (pure declarations)

### eval_overlap_mask
- Purpose: Convert vertex overlap mask to OverlapType
- Calls: None

### eval_overlap_collision
- Purpose: Convert cast result to OverlapType
- Calls: None

## Globals
- **COLLISION_EPSILON (float)**: Precision threshold for collision tests
- **Stats (ColmathStatsStruct)**: Global statistics tracker

## Dependencies
- "always.h", "vector3.h", "castres.h"
- CastResultStruct (forward reference)
