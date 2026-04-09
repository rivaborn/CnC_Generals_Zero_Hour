# GeneralsMD/Code/GameEngine/Include/Common/BezFwdIterator.h

## Purpose
Defines a forward iterator for Bezier curves, managing step-by-step traversal of a Bezier segment.

## Responsibilities
- Iterate through a Bezier segment in discrete steps
- Calculate current point and derivatives at each step
- Provide start/done/next interface for iteration control

## Key Types
- **BezFwdIterator (Class)**: Forward iterator for Bezier segments
- **BezierSegment (Class)**: Bezier segment being iterated (external)
- **Coord3D (Struct)**: 3D coordinate point (external)

## Key Functions
### BezFwdIterator(Int stepsDesired, const BezierSegment *bezSeg)
- Purpose: Constructs iterator with specified step count and Bezier segment
- Calls: None

### start()
- Purpose: Initializes iteration at the start of the Bezier segment
- Calls: None

### done()
- Purpose: Checks if iteration has completed
- Calls: None

### getCurrent()
- Purpose: Returns current 3D point in iteration
- Calls: None

### next()
- Purpose: Advances iteration to next step
- Calls: None

## Globals
None

## Dependencies
- **BezierSegment.h**: Defines BezierSegment class
- **Coord3D**: 3D coordinate type (assumed from context)
- **Int/Bool**: Basic integer and boolean types
