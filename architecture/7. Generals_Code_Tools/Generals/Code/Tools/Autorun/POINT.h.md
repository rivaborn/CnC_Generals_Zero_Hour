# Generals/Code/Tools/Autorun/POINT.h

## Purpose
Defines 2D and 3D point/vector classes with arithmetic and geometric operations.

## Responsibilities
- Provides template-based 2D and 3D point/vector classes
- Implements vector math operations (dot product, cross product, normalization)
- Supports arithmetic operations (+, -, *, /) for points/vectors
- Defines utility functions for distance and cross product calculations
- Maintains backward compatibility with legacy Point2DStruct

## Key Types
- **Point2DStruct (struct)**: Legacy 2D point structure with X/Y integers
- **TRect (class)**: Forward-declared 2D rectangle class (not implemented here)
- **TPoint2D<T> (class)**: Template 2D point/vector with arithmetic and vector operations
- **Point2D (class)**: Integer specialization of TPoint2D for 2D points
- **TPoint3D<T> (class)**: Template 3D point/vector inheriting from TPoint2D
- **Point3D (typedef)**: Integer specialization of TPoint3D for 3D points
- **BASECLASS (typedef)**: Internal typedef for TPoint2D base class in TPoint3D

## Key Functions
### Distance<T>(TPoint2D<T> const &, TPoint2D<T> const &)
- Purpose: Calculates Euclidean distance between two 2D points
- Calls: TPoint2D::operator-, TPoint2D::Length

### Cross_Product<T>(TPoint2D<T> const &, TPoint2D<T> const &)
- Purpose: Computes 2D cross product of two vectors
- Calls: TPoint2D::Cross_Product

### Cross_Product<T>(TPoint3D<T> const &, TPoint3D<T> const &)
- Purpose: Computes 3D cross product of two vectors
- Calls: TPoint3D::Cross_Product

## Globals
- None

## Dependencies
- `<math.h>` for sqrt function
- Uses double for intermediate calculations in Length/Normalize methods
- Assumes integer division semantics for template type T
