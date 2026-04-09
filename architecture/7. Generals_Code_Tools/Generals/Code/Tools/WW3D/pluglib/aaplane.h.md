# Generals/Code/Tools/WW3D/pluglib/aaplane.h

## Purpose
Defines a class representing axis-aligned planes for 3D math operations.

## Responsibilities
- Represents planes aligned to coordinate axes (X, Y, or Z)
- Stores plane normal direction and distance from origin
- Provides methods to set and retrieve plane properties

## Key Types
- **AAPlaneClass (Class)**: Represents an axis-aligned plane with normal and distance.
- **AxisEnum (Enum)**: Defines plane normal directions (XNORMAL, YNORMAL, ZNORMAL).

## Key Functions
### AAPlaneClass::Set
- Purpose: Sets the plane's normal and distance.
- Calls: None.

### AAPlaneClass::Get_Normal
- Purpose: Retrieves the plane's normal vector.
- Calls: Vector3::Set.

## Globals
- None.

## Dependencies
- `always.h` (header guards)
- `vector3.h` (Vector3 class)
