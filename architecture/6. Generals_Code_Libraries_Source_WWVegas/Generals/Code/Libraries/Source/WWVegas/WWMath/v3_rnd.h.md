# Generals/Code/Libraries/Source/WWVegas/WWMath/v3_rnd.h

## Purpose
Defines abstract and concrete classes for generating random 3D vectors within geometric shapes (box, sphere, cylinder).

## Responsibilities
- Provides abstract base class `Vector3Randomizer` for random vector generation
- Implements concrete randomizers for solid/hollow spheres, solid boxes, and solid cylinders
- Manages random number generation utilities for vector components
- Supports scaling and cloning of randomizers

## Key Types
- **Vector3Randomizer (Class)**: Abstract base class for random vector generation
- **Vector3SolidBoxRandomizer (Class)**: Generates points uniformly inside a box
- **Vector3SolidSphereRandomizer (Class)**: Generates points uniformly inside a sphere
- **Vector3HollowSphereRandomizer (Class)**: Generates points uniformly on a sphere's surface
- **Vector3SolidCylinderRandomizer (Class)**: Generates points uniformly inside a cylinder
- **CLASSID_* (Enum)**: Class IDs for RTTI (e.g., `CLASSID_SOLIDBOX`, `CLASSID_SOLIDSPHERE`)

## Key Functions
### `Get_Vector(Vector3 &vector)`
- Purpose: Fills `vector` with a randomly generated point within the shape
- Calls: `Get_Random_Float_Minus1_To_1()`, `Get_Random_Float_0_To_1()`

### `Get_Maximum_Extent()`
- Purpose: Returns the maximum possible component value for generated vectors
- Calls: None

### `Scale(float scale)`
- Purpose: Scales all future generated vectors by `scale`
- Calls: None

### `Clone()`
- Purpose: Creates a deep copy of the randomizer
- Calls: Constructor of derived class

## Globals
- **OOIntMax (float)**: Constant for random float conversion
- **OOUIntMax (float)**: Constant for random float conversion
- **Randomizer (Random3Class)**: Static random number generator

## Dependencies
- `vector3.h` (Vector3)
- `random.h` (Random3Class)
- `always.h` (W3DNEW macro)
