# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/euler.h

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
### EulerAnglesClass::EulerAnglesClass (default constructor)
- Purpose: Initializes angles to zero and order to 0.
- Calls: None.

### EulerAnglesClass::EulerAnglesClass (Matrix3D, int)
- Purpose: Constructs from a matrix using a specified rotation order.
- Calls: `From_Matrix`.

### EulerAnglesClass::From_Matrix
- Purpose: Extracts Euler angles from a 3D matrix given a rotation order.
- Calls: Not inferable.

### EulerAnglesClass::To_Matrix
- Purpose: Converts Euler angles back into a 3D matrix.
- Calls: Not inferable.

### EulerAnglesClass::Get_Angle
- Purpose: Retrieves a specific angle by index.
- Calls: None.

## Globals
- **EulerOrderXYZs (int)**: Static XYZ rotation order constant.
- **EulerOrderXYXs (int)**: Static XYX rotation order constant.
- **EulerOrderXZYs (int)**: Static XZY rotation order constant.
- **EulerOrderXZXs (int)**: Static XZX rotation order constant.
- **EulerOrderYZXs (int)**: Static YZX rotation order constant.
