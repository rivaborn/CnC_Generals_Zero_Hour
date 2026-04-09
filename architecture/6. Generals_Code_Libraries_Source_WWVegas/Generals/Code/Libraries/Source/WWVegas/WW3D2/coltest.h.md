# Generals/Code/Libraries/Source/WWVegas/WW3D2/coltest.h

## Purpose
Defines collision test classes for ray, axis-aligned box (AABB), and oriented bounding box (OBB) collision detection in the SAGE engine.

## Responsibilities
- Provides base `CollisionTestClass` and derived classes for different collision test types
- Implements culling and triangle intersection tests for each collision type
- Manages collision result storage and transformation of collision tests
- Supports movement and rotation of collision volumes

## Key Types
- **RenderObjClass (Class)**: Reference to collided render object (not defined here)
- **CollisionTestClass (Class)**: Base class for collision tests, holds result pointer and collision type
- **RayCollisionTestClass (Class)**: Ray-line segment collision test
- **AABoxCollisionTestClass (Class)**: Axis-aligned box sweep collision test
- **ROTATION_TYPE (Enum)**: Rotation flags (0Â°, 90Â°, 180Â°, 270Â° around Z-axis)
- **OBBoxCollisionTestClass (Class)**: Oriented bounding box sweep collision test

## Key Functions
### CollisionTestClass::CollisionTestClass
- Purpose: Constructs base collision test with result pointer and type
- Calls: None

### RayCollisionTestClass::Cast_To_Triangle
- Purpose: Tests ray-triangle intersection
- Calls: `CollisionMath::Collide`

### AABoxCollisionTestClass::Cast_To_Triangle
- Purpose: Tests swept AABB-triangle intersection
- Calls: `CollisionMath::Collide`

### OBBoxCollisionTestClass::Cast_To_Triangle
- Purpose: Tests swept OBB-triangle intersection
- Calls: `CollisionMath::Collide`

## Globals
- None

## Dependencies
- `always.h`, `castres.h`, `lineseg.h`, `aabox.h`, `obbox.h`, `tri.h`, `colmath.h`, `coltype.h`
- `Vector3`, `Matrix3D`, `CollisionMath`, `CastResultStruct`
