# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/v3_rnd.cpp

## Purpose
Implements random vector generation within geometric shapes (box, sphere, cylinder) for 3D math operations.

## Responsibilities
- Generates random vectors within solid/hollow spheres, boxes, and cylinders
- Provides scaling and extent calculation for randomizers
- Uses rejection sampling for shape-constrained randomness

## Key Types
- **Vector3SolidBoxRandomizer (Class)**: Generates random vectors within an axis-aligned box
- **Vector3SolidSphereRandomizer (Class)**: Generates random vectors within a solid sphere
- **Vector3HollowSphereRandomizer (Class)**: Generates random vectors on a sphere's surface
- **Vector3SolidCylinderRandomizer (Class)**: Generates random vectors within a solid cylinder
- **Vector3Randomizer (Class)**: Base class providing random float generation

## Key Functions
### `Get_Vector`
- Purpose: Fills a Vector3 with a random point within the shape's bounds
- Calls: `Get_Random_Float_Minus1_To_1()`, `Length2()`, `WWMath::Inv_Sqrt()`

### `Get_Maximum_Extent`
- Purpose: Returns the maximum distance from origin to any point in the shape
- Calls: None

### `Scale`
- Purpose: Scales the shape's dimensions by a factor
- Calls: None

## Globals
- **Vector3Randomizer::OOIntMax (float)**: Conversion factor for INT_MAX
- **Vector3Randomizer::OOUIntMax (float)**: Conversion factor for UINT_MAX
- **Vector3Randomizer::Randomizer (Random3Class)**: Global random number generator

## Dependencies
- `v3_rnd.h`, `vector2.h`
- `Vector3`, `Vector2` classes
-
