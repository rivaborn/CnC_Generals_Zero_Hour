# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.cpp

## Purpose
Implements vehicle pathfinding curves using arc-based interpolation for smooth movement.

## Responsibilities
- Calculates turn arcs and tangent points for vehicle paths
- Manages curve evaluation and sharpness detection
- Handles serialization of curve data

## Key Types
- `VehicleCurveClass` (Class): Main curve class handling path evaluation
- `ArcInfoStruct` (Struct): Stores arc segment data (center, angles, points)
- `CHUNKID_*` (Enum): Chunk IDs for save/load operations

## Key Functions
### `Find_Tangent`
- Purpose: Computes tangent points from a circle to a given point
- Calls: `WWMath::Acos`, `WWMath::Atan2`, `WWMath::Wrap`

### `Get_Angle_Delta`
- Purpose: Calculates angle difference considering clockwise/counter-clockwise orientation
- Calls: None

### `Find_Turn_Arc`
- Purpose: Determines optimal turn arc center and direction
- Calls: `WWMath::Atan2`, `WWMath::Wrap`, `Matrix3D::Inverse_Transform_Vector`

### `Find_Tangents`
- Purpose: Computes entry/exit tangent angles for a turn arc
- Calls: `Find_Tangent`, `Get_Angle_Delta`

### `Update_Arc_List`
- Purpose: Rebuilds arc information when curve keys change
- Calls: `Find_Turn_Arc`, `Find_Tangents`

### `Evaluate`
- Purpose: Evaluates curve position at a given time
- Calls: `Find_Interval`, `WWMath::Clamp`

## Globals
- `_VehicleCurveFactory` (SimplePersistFactoryClass): Factory for serialization

## Dependencies
- `vehiclecurve.h`, `vector3.h`, `matrix3d.h`, `persistfactory.h`
- `WWMath` namespace functions (trigonometry, wrapping)
- `Curve3DClass` base class methods
