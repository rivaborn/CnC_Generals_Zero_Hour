# GeneralsMD/Code/GameEngine/Source/Common/Bezier/BezierSegment.cpp

## Purpose
Implements a BÃ©zier curve segment with evaluation, length approximation, and splitting functionality.

## Responsibilities
- Constructs BÃ©zier segments from various input formats
- Evaluates points on the curve at parameter `t`
- Approximates curve length with recursive subdivision
- Splits segments at a given parameter value

## Key Types
- **BezierSegment (Class)**: Represents a cubic BÃ©zier curve segment with 4 control points
- **Coord3D (Struct)**: 3D coordinate point (external)
- **D3DXVECTOR4/D3DXMATRIX (Types)**: Direct3D vector/matrix types (external)

## Key Functions
### `evaluateBezSegmentAtT`
- Purpose: Computes the point on the curve at parameter `t`
- Calls: `D3DXVec4Transform`, `D3DXVec4Dot`

### `getApproximateLength`
- Purpose: Recursively approximates the curve's length
- Calls: `splitSegmentAtT`, `length()` (on Coord3D)

### `splitSegmentAtT`
- Purpose: Subdivides the segment into two at parameter `t`
- Calls: `evaluateBezSegmentAtT`, `scale`, `add` (on Coord3D)

## Globals
- **s_bezBasisMatrix (D3DXMATRIX)**: Static basis matrix for BÃ©zier evaluation

## Dependencies
- `Common/BezierSegment.h`, `Common/BezFwdIterator.h`
- `<D3DX8Math.h>` (Direct3D math library)
- `Coord3D` struct, `VecCoord3D` container (external)
