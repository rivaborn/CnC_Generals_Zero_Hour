# Generals/Code/GameEngine/Source/Common/Bezier/BezFwdIterator.cpp

## Purpose
This file implements a forward iterator for Bezier curves, allowing traversal of curve points in a specified number of steps.

## Responsibilities
- Initialize and configure the iterator with desired steps and a Bezier segment.
- Start the iteration process by calculating initial derivatives.
- Check if the iteration is complete.
- Retrieve the current point on the curve.
- Move to the next point in the sequence.

## Key Types
- None

## Key Functions
### BezFwdIterator::BezFwdIterator()
- Purpose: Default constructor initializes member variables.
- Calls: None

### BezFwdIterator::BezFwdIterator(Int stepsDesired, const BezierSegment *bezSeg)
- Purpose: Constructor initializes with desired steps and a Bezier segment.
- Calls: None

### BezFwdIterator::start()
- Purpose: Prepares the iterator for traversal by calculating initial derivatives.
- Calls: D3DXVec4Transform, add methods on vectors

### BezFwdIterator::done()
- Purpose: Checks if the iteration is complete.
- Calls: None

### BezFwdIterator::getCurrent()
- Purpose: Retrieves the current point on the curve.
- Calls: None

### BezFwdIterator::next()
- Purpose: Moves to the next point in the sequence by updating derivatives and position.
- Calls: add methods on vectors

## Globals
- None

## Dependencies
- Key includes: "PreRTS.h", "Common/BezFwdIterator.h"
- External symbols used: BezierSegment, D3DXVECTOR4, D3DXVec4Transform, Coord3D
