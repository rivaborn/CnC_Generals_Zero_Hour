# GeneralsMD/Code/GameEngine/Source/Common/Bezier/BezFwdIterator.cpp

## Purpose
Implements a forward iterator for Bezier curves, allowing step-by-step traversal of curve points.

## Responsibilities
- Initializes iterator state
- Computes curve derivatives for interpolation
- Advances to next point in curve
- Checks iteration completion

## Key Types
- **BezFwdIterator (Class)**: Iterates over Bezier curve segments
- **BezierSegment (Class)**: Bezier curve segment (referenced, not defined here)
- **Coord3D (Struct)**: 3D coordinate point

## Key Functions
### BezFwdIterator()
- Purpose: Default constructor initializing member variables
- Calls: None

### BezFwdIterator(Int, const BezierSegment*)
- Purpose: Constructor initializing with desired steps and curve segment
- Calls: None

### start()
- Purpose: Initializes iteration state and computes curve derivatives
- Calls: D3DXVec4Transform (DirectX math library)

### done()
- Purpose: Checks if iteration is complete
- Calls: None

### getCurrent()
- Purpose: Returns current point in iteration
- Calls: None

### next()
- Purpose: Advances to next point in curve
- Calls: None

## Globals
None

## Dependencies
- "Common/BezFwdIterator.h" (header)
- "PreRTS.h" (precompiled header)
- D3DXVECTOR4, D3DXVec4Transform (DirectX math)
- BezierSegment::s_bezBasisMatrix (static matrix)
