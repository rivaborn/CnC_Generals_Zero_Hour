# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/sphere.h

## Purpose
Defines the `SphereClass` for 3D sphere operations, including intersection tests, transformations, and bounding volume calculations.

## Responsibilities
- Represents 3D spheres with center and radius
- Provides sphere-sphere intersection tests
- Supports sphere transformations and combinations
- Computes bounding spheres from vertex sets

## Key Types
- **SphereClass (Class)**: Encapsulates a 3D sphere with center (Vector3) and radius (float)
- **None**: No enums/structs beyond the class

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

### operator+ (SphereClass)
- Purpose: Combines two spheres into an enclosing sphere
- Calls: Add_Spheres

### operator* (Matrix3D, SphereClass)
- Purpose: Transforms a sphere by a matrix
- Calls: Transform_Sphere

## Globals
- **None**

## Dependencies
- `vector3.h` (Vector3 class)
- `matrix3d.h` (Matrix3D class)
- `always.h` (ALLOW_TEMPORARIES flag)
