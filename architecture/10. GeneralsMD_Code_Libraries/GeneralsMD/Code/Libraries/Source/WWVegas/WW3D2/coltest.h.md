# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/coltest.h

## Purpose
Defines collision test classes for ray, axis-aligned box (AABB), and oriented bounding box (OBB) collision detection in the SAGE engine.

## Responsibilities
- Provides base `CollisionTestClass` and derived classes for different collision test types.
- Implements culling and triangle intersection tests for each collision type.
- Supports transformation (translation/rotation) of collision tests.
- Manages collision result storage via `CastResultStruct`.

## Key Types
- **CollisionTestClass (Class)**: Base class for collision tests, holds result pointer and collision type.
- **RayCollisionTestClass (Class)**: Tests ray-line segment collisions with optional translucent/hidden checks.
- **AABoxCollisionTestClass (Class)**: Tests axis-aligned box collisions with sweep volume.
- **OBBoxCollisionTestClass (Class)**: Tests oriented bounding box collisions with sweep volume.
- **ROTATION_TYPE (Enum)**: Defines 90Â° rotation increments (0Â°, 90Â°, 180Â°, 270Â°).

## Key Functions
### `Cull(const Vector3 & min, const Vector3 & max)`
- Purpose: Fast spatial culling using min/max bounds.
- Calls: `CollisionMath::Overlap_Test` (for `RayCollisionTestClass`).

### `Cast_To_Triangle(const TriClass & tri)`
- Purpose: Performs precise collision test against a triangle.
- Calls: `CollisionMath::Collide` (for all derived classes).

### `Translate/Rotate/Transform`
- Purpose: Modifies collision test geometry (only in `AABoxCollisionTestClass`).
- Calls: None (inline operations).

## Globals
- **RenderObjClass** (pointer): Stored in base class for collision object reference.

## Dependencies
- **Includes**: `always.h`, `castres.h`, `lineseg.h`, `aabox.h`, `obbox.h`, `tri.h`, `colmath.h`, `coltype.h`.
- **Externals**: `CollisionMath`, `Vector3`, `Matrix3D`, `CastResultStruct`.
