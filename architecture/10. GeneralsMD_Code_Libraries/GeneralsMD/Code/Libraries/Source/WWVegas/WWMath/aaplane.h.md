# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/aaplane.h

## Purpose
Defines a class representing axis-aligned planes for mathematical operations in the game engine.

## Responsibilities
- Represents planes aligned to one of the three coordinate axes (X, Y, or Z).
- Provides methods to set and retrieve the plane's normal vector.
- Stores the plane's distance from the origin.

## Key Types
- **AAPlaneClass (Class)**: Represents an axis-aligned plane with a normal vector along one of the coordinate axes.
- **AxisEnum (Enum)**: Defines the three possible axis-aligned normals (X, Y, Z).
- **XNORMAL (Enum)**: Represents the X-axis normal.
- **YNORMAL (Enum)**: Represents the Y-axis normal.
- **ZNORMAL (Enum)**: Represents the Z-axis normal.

## Key Functions
### AAPlaneClass::Set
- Purpose: Sets the plane's normal and distance.
- Calls: None.

### AAPlaneClass::Get_Normal
- Purpose: Retrieves the plane's normal vector.
- Calls: `Vector3::Set`.

## Globals
- None.

## Dependencies
- `always.h`: Likely contains common macros or definitions.
- `vector3.h`: Defines the `Vector3` class used for normal vectors.
- `Vector3`: Used to return the normal vector in `Get_Normal`.
