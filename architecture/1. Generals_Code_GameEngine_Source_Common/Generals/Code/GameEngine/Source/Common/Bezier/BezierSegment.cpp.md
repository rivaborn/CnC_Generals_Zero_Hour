# Generals/Code/GameEngine/Source/Common/Bezier/BezierSegment.cpp

## Purpose
This file implements the `BezierSegment` class, which represents a cubic Bezier curve segment in 3D space. It provides methods to evaluate points on the curve, calculate its length, and split it at a given parameter.

## Responsibilities
- Representing a cubic Bezier curve with four control points.
- Evaluating points on the curve at a specific parameter `t`.
- Calculating an approximate length of the curve segment.
- Splitting the curve into two segments at a specified parameter `t`.

## Key Types
- **BezierSegment (Class)**: Represents a cubic Bezier curve segment.
- **Coord3D (Struct)**: Represents a 3D coordinate.
- **VecCoord3D (Class)**: A vector of `Coord3D` points.

## Key Functions
### BezierSegment::evaluateBezSegmentAtT
- Purpose: Evaluates the point on the Bezier curve at parameter `t`.
- Calls:
  - D3DXVec4Transform
  - D3DXVec4Dot

### BezierSegment::getSegmentPoints
- Purpose: Generates a set of points along the curve.
- Calls:
  - BezFwdIterator::start
  - BezFwdIterator::next
  - BezFwdIterator::done

### BezierSegment::getApproximateLength
- Purpose: Calculates an approximate length of the Bezier segment within a specified tolerance.
- Calls:
  - splitSegmentAtT (recursively)

### BezierSegment::splitSegmentAtT
- Purpose: Splits the Bezier curve into two segments at parameter `t`.
- Calls:
  - evaluateBezSegmentAtT

## Globals
- **s_bezBasisMatrix (D3DXMATRIX)**: The basis matrix for evaluating cubic Bezier curves.

## Dependencies
- **Common/BezierSegment.h**: Header file for the `BezierSegment` class.
- **Common/BezFwdIterator.h**: Header file for the forward iterator used to generate points on the curve.
- **D3DX8Math.h**: Direct3D math library for vector operations.
