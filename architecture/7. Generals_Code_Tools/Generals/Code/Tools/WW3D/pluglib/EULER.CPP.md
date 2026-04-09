# Generals/Code/Tools/WW3D/pluglib/EULER.CPP

## Purpose
Implements Euler angle conversions for 3D rotation matrices, supporting 24 possible Euler angle conventions.

## Responsibilities
- Convert between 3x3 rotation matrices and Euler angles
- Handle 24 different Euler angle conventions (static/rotating frames, parity, repeat)
- Provide utility functions for axis extraction from Euler orders
- Manage matrix/array conversions for internal calculations

## Key Types
- **EulerAnglesClass (Class)**: Wraps Euler angle calculations and conversions
- **Matrix3 (External)**: 3x3 transformation matrix type
- **Point3 (External)**: 3D point/vector type

## Key Functions
### `EulerAnglesClass::From_Matrix`
- Purpose: Extracts Euler angles from a rotation matrix given a specific convention
- Calls: `_euler_unpack_order`, `_mat_to_array`, `atan2`, `sqrt`

### `EulerAnglesClass::To_Matrix`
- Purpose: Converts Euler angles back into a rotation matrix
- Calls: `_euler_unpack_order`, `_array_to_mat`, `cos`, `sin`

### `_euler_unpack_order`
- Purpose: Decodes Euler order into component flags (axes, parity, repeat, frame)
- Calls: None

### `_mat_to_array` / `_array_to_mat`
- Purpose: Converts between Matrix3 and float array representations
- Calls: `Matrix3::GetRow`, `Matrix3::SetRow`

## Globals
- **EulerOrderXYZs/XZYs/etc. (int)**: Predefined Euler order constants for all 24 conventions
- **_euler_safe/_euler_next (int[])**: Lookup tables for axis ordering

## Dependencies
- `euler.h` (header)
- `float.h` (for FLT_EPSILON)
- `Matrix3`, `Point3` (external 3D math types)
