# Generals/Code/Libraries/Source/WWVegas/WWMath/frustum.h

## Purpose
Defines the `FrustumClass` for representing a view frustum in 3D space, used for visibility culling.

## Responsibilities
- Stores frustum planes, corners, and bounds
- Provides initialization from camera and viewport parameters
- Exposes accessors for bound min/max

## Key Types
- **FrustumClass (Class)**: Represents a view frustum with planes, corners, and bounds

## Key Functions
### FrustumClass::Init
- Purpose: Initializes the frustum from camera transform and viewport parameters
- Calls: Not inferable (implementation in .cpp)

### FrustumClass::Get_Bound_Min
- Purpose: Returns the minimum bound of the frustum
- Calls: None

### FrustumClass::Get_Bound_Max
- Purpose: Returns the maximum bound of the frustum
- Calls: None

## Globals
- None

## Dependencies
- `vector3.h` (Vector3, Vector2)
- `plane.h` (PlaneClass)
- `Matrix3D` (external)
