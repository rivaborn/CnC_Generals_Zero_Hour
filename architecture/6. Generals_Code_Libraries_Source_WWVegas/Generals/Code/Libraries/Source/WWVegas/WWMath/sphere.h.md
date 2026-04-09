# Generals/Code/Libraries/Source/WWVegas/WWMath/sphere.h

## Purpose
Defines the SphereClass for 3D sphere operations, including intersection tests, transformations, and bounding volume calculations.

## Responsibilities
- Represents 3D spheres with center and radius
- Provides sphere-sphere intersection tests
- Supports sphere transformations and combinations
- Calculates bounding spheres from vertex sets
- Implements sphere volume calculation

## Key Types
- **SphereClass (Class)**: Encapsulates a 3D sphere with center (Vector3) and radius (float)
- **Vector3 (Struct)**: 3D vector used for sphere centers (external)
- **Matrix3D (Struct)**: 3D transformation matrix (external)

## Key Functions
### Spheres_Intersect
- Purpose: Tests if two spheres intersect
- Calls: Vector3::Dot_Product

### Add_Spheres
- Purpose: Creates a new sphere enclosing two input spheres
- Calls: SphereClass::Add_Sphere

### Transform_Sphere (overloads)
- Purpose: Transforms a sphere by a matrix
- Calls: Matrix3D::mulVector3 (conditional)

### SphereClass::Add_Sphere
- Purpose: Expands sphere to enclose another sphere
- Calls: None

### SphereClass::Transform
- Purpose: Applies matrix transformation to sphere center
- Calls: Matrix3D::mulVector3 (conditional)

## Globals
None

## Dependencies
- "vector3.h" (Vector3)
- "matrix3d.h" (Matrix3D)
- "always.h" (WWMATH_PI constant)
