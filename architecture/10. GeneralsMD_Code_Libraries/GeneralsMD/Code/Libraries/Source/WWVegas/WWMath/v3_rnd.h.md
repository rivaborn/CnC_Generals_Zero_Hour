# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/v3_rnd.h

## Purpose
Defines abstract and concrete classes for generating random 3D vectors within geometric shapes (box, sphere, cylinder).

## Responsibilities
- Provide base class `Vector3Randomizer` for random vector generation
- Implement concrete randomizers for box, sphere (solid/hollow), and cylinder
- Support scaling and cloning of randomizers
- Use RTTI via `Class_ID()` for type identification

## Key Types
- **Vector3Randomizer (Class)**: Abstract base class for random vector generation
- **Vector3SolidBoxRandomizer (Class)**: Generates points in a box centered at origin
- **Vector3SolidSphereRandomizer (Class)**: Generates points inside a sphere
- **Vector3HollowSphereRandomizer (Class)**: Generates points on a sphere's surface
- **Vector3SolidCylinderRandomizer (Class)**: Generates points inside a cylinder
- **CLASSID_* (Enum)**: RTTI identifiers for randomizer types

## Key Functions
### `Get_Vector(Vector3 &vector)`
- Purpose: Fills `vector` with a randomly generated point
- Calls: `Get_Random_Float_Minus1_To_1()`, `Get_Random_Float_0_To_1()`

### `Scale(float scale)`
- Purpose: Scales all future generated vectors by `scale`
- Calls: None

### `Clone()`
- Purpose: Creates a deep copy of the randomizer
- Calls: Copy constructor of derived class

## Globals
- **OOIntMax (float)**: Constant for random float in [-1, 1]
- **OOUIntMax (float)**: Constant for random float in [0, 1]
- **Randomizer (Random3Class)**: Static random number generator

## Dependencies
- `vector3.h` (Vector3)
- `random.h` (Random3Class)
- `always.h` (W3DNEW macro)
