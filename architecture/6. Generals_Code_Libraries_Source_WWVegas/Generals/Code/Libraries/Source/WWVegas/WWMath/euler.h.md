# Generals/Code/Libraries/Source/WWVegas/WWMath/euler.h

## Purpose
Defines the `EulerAnglesClass` for converting between 3D matrices and Euler angles using various rotation conventions.

## Responsibilities
- Provide Euler angle representation and conversion utilities
- Support multiple rotation order conventions (static/rotating axes)
- Convert between `Matrix3D` and Euler angles
- Expose angle retrieval methods

## Key Types
- **EulerAnglesClass (Class)**: Wraps Euler angle data and conversion logic for 3D matrices.

## Key Functions
### `EulerAnglesClass::From_Matrix`
- Purpose: Converts a `Matrix3D` into Euler angles using a specified rotation order.
- Calls: Not inferable.

### `EulerAnglesClass::To_Matrix`
- Purpose: Converts Euler angles back into a `Matrix3D`.
- Calls: Not inferable.

### `EulerAnglesClass::Get_Angle`
- Purpose: Retrieves an individual Euler angle by index.
- Calls: Not inferable.

## Globals
- **EulerOrderXYZs (int)**: Static XYZ rotation order constant.
- **EulerOrderXYXr (int)**: Rotating XYX rotation order constant.
- (19 other similar constants for different rotation orders)

## Dependencies
- `always.h`, `matrix3d.h`, `quat.h`
- Uses `Matrix3D` class (external).
