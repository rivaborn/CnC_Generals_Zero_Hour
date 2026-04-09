# Generals/Code/Tools/WW3D/pluglib/EULER.H

## Purpose
Defines Euler angle rotation conventions and a class for converting between matrices and Euler angles.

## Responsibilities
- Declares Euler order constants for static and rotating axes
- Provides `EulerAnglesClass` for matrix-to-Euler and Euler-to-matrix conversions
- Exposes angle retrieval methods

## Key Types
- `EulerAnglesClass` (Class): Wraps Euler angle data and conversion logic
- `EulerOrderXYZs`, `EulerOrderXYXs`, etc. (int): Predefined static axis rotation orders
- `EulerOrderXYZr`, `EulerOrderXYXr`, etc. (int): Predefined rotating axis rotation orders

## Key Functions
### `EulerAnglesClass::From_Matrix`
- Purpose: Converts a 3x3 matrix into Euler angles using a specified order
- Calls: Not inferable

### `EulerAnglesClass::To_Matrix`
- Purpose: Converts Euler angles back into a 3x3 matrix
- Calls: Not inferable

### `EulerAnglesClass::Get_Angle`
- Purpose: Retrieves an individual Euler angle by index
- Calls: Not inferable

## Globals
- `EulerOrderXYZs`, `EulerOrderXYXs`, etc. (int): Static axis rotation order constants
- `EulerOrderXYZr`, `EulerOrderXYXr`, etc. (int): Rotating axis rotation order constants

## Dependencies
- `<Max.h>`: 3DS Max SDK header for `Matrix3`
- `Matrix3`: External matrix type used for conversions
