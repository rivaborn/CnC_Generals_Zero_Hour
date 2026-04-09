# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/euler.cpp

## Purpose
Implements Euler angle conversions between 3D matrices and angle representations.

## Responsibilities
- Defines Euler angle conventions (24 possible orders)
- Converts between Matrix3D and Euler angles
- Handles static/rotating frame transformations
- Provides utility functions for axis extraction

## Key Types
- `EulerAnglesClass`: Wraps Euler angle operations
- `Matrix3D`: 3x3 transformation matrix (external)

## Key Functions
### `EulerAnglesClass::From_Matrix`
- Purpose: Extracts Euler angles from a rotation matrix
- Calls: `_euler_unpack_order`, `WWMath::Atan2`

### `EulerAnglesClass::To_Matrix`
- Purpose: Constructs a rotation matrix from Euler angles
- Calls: `_euler_unpack_order`, `WWMath::Cos`, `WWMath::Sin`

### `_euler_unpack_order`
- Purpose: Decodes Euler order into axis indices
- Calls: `_euler_axis_i`, `_euler_axis_j`, `_euler_axis_k`, `_euler_axis_h`

## Globals
- `EulerOrderXYZs` (int): Static XYZ order constant
- `_euler_safe` (int[]): Axis mapping table
- `_euler_next` (int[]): Axis sequence table

## Dependencies
- `euler.h` (header)
- `Matrix3D` (external class)
- `WWMath` namespace (trigonometric functions)
