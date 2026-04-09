# GeneralsMD/Code/GameEngine/Include/Common/BezierSegment.h

## Purpose
Defines the `BezierSegment` class for handling BÃ©zier curve segments in 3D space.

## Responsibilities
- Manages control points for a cubic BÃ©zier segment.
- Provides evaluation, splitting, and length approximation of the curve.
- Supports iteration via a friend class (`BezFwdIterator`).

## Key Types
- **BezierSegment (Class)**: Represents a cubic BÃ©zier curve segment with 4 control points.

## Key Functions
### `evaluateBezSegmentAtT`
- Purpose: Computes the point on the curve at parameter `t`.
- Calls: Not inferable.

### `getSegmentPoints`
- Purpose: Generates discrete points approximating the curve.
- Calls: Not inferable.

### `getApproximateLength`
- Purpose: Estimates the curve's length within a tolerance.
- Calls: Not inferable.

### `splitSegmentAtT`
- Purpose: Splits the segment into two at parameter `t`.
- Calls: Not inferable.

## Globals
- **s_bezBasisMatrix (D3DXMATRIX)**: Static basis matrix for BÃ©zier calculations.
- **USUAL_TOLERANCE (Real)**: Default tolerance value for length approximation.

## Dependencies
- `<D3DX8Math.h>`: DirectX math library for vectors/matrices.
- `"Common/STLTypeDefs.h"`: Custom STL type definitions (`Coord3D`, `VecCoord3D`, `Real`).
