# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/normalcone.h

## Purpose
Defines the `NormalCone` class for representing a cone of unit-length normals, used for hierarchical backface culling.

## Responsibilities
- Represents a circular portion of a sphere (cone) of normals.
- Supports merging cones and normals to expand the cone.
- Provides methods to check containment and compute coplanar normals.
- Handles degenerate cases (hemisphere, full sphere).

## Key Types
- **NormalCone (Class)**: Extends `Vector3` to represent a cone of normals with an angle.
- **Vector3 (Class)**: Base class for 3D vectors.
- **Matrix3 (Class)**: Used for vector rotation.

## Key Functions
### `NormalCone::Merge(const Vector3 & Input)`
- Purpose: Expands the cone to include the input normal.
- Calls: `Complete_Sphere`, `Dot_Product`, `Get_Coplanar_Normals_And_Dots`, `Set`, `Normalize`.

### `NormalCone::Merge(const NormalCone & Input)`
- Purpose: Merges another cone's coplanar normals into this cone.
- Calls: `Get_Coplanar_Normals`, `Merge(const Vector3 &)`.

### `NormalCone::Smallest_Dot_Product(const Vector3 & Input)`
- Purpose: Returns the dot product with the nearest coplanar normal in the cone.
- Calls: `Complete_Sphere`, `Dot_Product`, `Get_Coplanar_Normals_And_Dots`.

### `NormalCone::Get_Coplanar_Normals(const Vector3 & Input, Vector3 & Output1, Vector3 & Output2)`
- Purpose: Computes two normals on the cone's edge coplanar with the input.
- Calls: `Cross_Product`, `Length2`, `Rotate_Vector`.

## Globals
- **WWMATH_EPSILON (float)**: Small value for floating-point comparisons.
- **WWMATH_PI (float)**: Value of Ï for angle calculations.

## Dependencies
- `vector3.h` (Vector3, Matrix3)
- `matrix3.h` (Matrix3)
