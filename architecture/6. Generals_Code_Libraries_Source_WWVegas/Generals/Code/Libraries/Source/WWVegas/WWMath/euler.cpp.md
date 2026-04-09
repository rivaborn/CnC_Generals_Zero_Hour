# Generals/Code/Libraries/Source/WWVegas/WWMath/euler.cpp

## Purpose
Implements Euler angle conversions between 3D matrices and angle representations.

## Responsibilities
- Converts between Matrix3D and Euler angles
- Supports 24 Euler angle conventions
- Handles static and rotating frame transformations
- Provides utility functions for axis extraction

## Key Types
- EulerAnglesClass (Class): Manages Euler angle conversions
- Matrix3D (External): 3x3 transformation matrix

## Key Functions
### EulerAnglesClass::From_Matrix
- Purpose: Computes Euler angles from a matrix
- Calls: _euler_unpack_order, WWMath::Atan2

### EulerAnglesClass::To_Matrix
- Purpose: Builds a matrix from Euler angles
- Calls: _euler_unpack_order, WWMath::Cos, WWMath::Sin

### _euler_unpack_order
- Purpose: Decodes Euler order into component axes
- Calls: _euler_axis_i, _euler_axis_j, _euler_axis_k, _euler_axis_h

## Globals
- EulerOrderXYZs (int): Static XYZ order constant
- EulerOrderZYXr (int): Rotating ZYX order constant
- _euler_safe (int[]): Axis mapping array
- _euler_next (int[]): Axis sequence array

## Dependencies
- euler.h (header)
- float.h (for FLT_EPSILON)
- Matrix3D class
- WWMath namespace (Atan2, Cos, Sin)
