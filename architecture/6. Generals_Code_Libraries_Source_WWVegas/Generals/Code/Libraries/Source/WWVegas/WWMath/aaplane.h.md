# Generals/Code/Libraries/Source/WWVegas/WWMath/aaplane.h

## Purpose
Defines a class representing axis-aligned planes for mathematical operations in the game engine.

## Responsibilities
- Represents planes aligned to one of the three coordinate axes (X, Y, or Z).
- Provides methods to set and retrieve plane properties.
- Stores the normal axis and distance from origin.

## Key Types
- **AAPlaneClass (Class)**: Represents an axis-aligned plane with a normal and distance.
- **AxisEnum (Enum)**: Defines the three possible normal axes (X, Y, Z).
- **XNORMAL (Enum)**: Constant for X-axis normal.
- **YNORMAL (Enum)**: Constant for Y-axis normal.
- **ZNORMAL (Enum)**: Constant for Z-axis normal.

## Key Functions
### AAPlaneClass::Set
- Purpose: Sets the normal axis and distance of the plane.
- Calls: None.

### AAPlaneClass::Get_Normal
- Purpose: Retrieves the normal vector of the plane.
- Calls: `Vector3::Set`.

## Globals
- None.

## Dependencies
- `always.h`: Likely contains common macros or definitions.
- `vector3.h`: Defines the `Vector3` class used for normal vectors.
