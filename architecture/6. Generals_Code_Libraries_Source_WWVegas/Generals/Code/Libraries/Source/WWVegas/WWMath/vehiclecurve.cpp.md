# Generals/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.cpp

## Purpose
Implements vehicle pathfinding curves using arc-based interpolation for smooth movement.

## Responsibilities
- Calculates tangent points and turn arcs for vehicle paths
- Manages curve evaluation and sharpness detection
- Handles serialization of curve data

## Key Types
- `VehicleCurveClass` (Class): Main curve class handling path evaluation
- `ArcInfoStruct` (Struct): Stores arc segment data (center, angles, points)
- `CHUNKID_*` (Enums): Chunk IDs for save/load operations
- `VARID_*` (Enums): Variable IDs for serialization

## Key Functions
### `Find_Tangent`
- Purpose: Calculates tangent points from a circle to an external point
- Calls: `WWMath::Acos`, `WWMath::Atan2`, `WWMath::Wrap`

### `Get_Angle_Delta`
- Purpose: Computes angle differences considering clockwise/counter-clockwise orientation
- Calls: None (pure math)

### `Find_Turn_Arc`
- Purpose: Determines the center and direction of a turn arc between three points
- Calls: `WWMath::Atan2`, `WWMath::Wrap`, `Matrix3D::Inverse_Transform_Vector`

### `Find_Tangents`
- Purpose: Computes entry/exit tangent angles for a turn arc
- Calls: `Find_Tangent`, `Get_Angle_Delta`

### `Update_Arc_List`
- Purpose: Recalculates all arc segments when curve keys change
- Calls: `Find_Turn_Arc`, `Find_Tangents`

### `Evaluate`
- Purpose: Evaluates the curve at a specific time to get position
- Calls: `Find_Interval`, `WWMath::Clamp`

## Globals
- `_VehicleCurveFactory` (SimplePersistFactoryClass): Factory for serialization

## Dependencies
- `vehiclecurve.h`, `vector3.h`, `matrix3d.h`, `persistfactory.h`, `wwmathids.h`, `wwmemlog.h`
- `WWMath` namespace functions (trig, vector ops)
- `Curve3DClass` (parent class)
