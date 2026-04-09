# Generals/Code/Libraries/Source/WWVegas/WWMath/curve.cpp

## Purpose
Implements 1D and 3D curve classes for animation and interpolation, including persistence support.

## Responsibilities
- Manages keyframe-based curves (1D and 3D)
- Handles linear interpolation between keys
- Provides serialization/deserialization for save/load
- Supports looping curves
- Factory registration for persistence system

## Key Types
- Curve3DClass (Class): Base class for 3D curves with keyframe support
- LinearCurve3DClass (Class): Linear interpolation 3D curve
- Curve1DClass (Class): Base class for 1D curves with keyframe support
- LinearCurve1DClass (Class): Linear interpolation 1D curve
- (anonymous enum) (Enum): Chunk ID constants for serialization

## Key Functions
### Curve3DClass::Find_Interval
- Purpose: Finds the interval containing a given time
- Calls: None

### LinearCurve3DClass::Evaluate
- Purpose: Evaluates the curve at a given time
- Calls: Curve3DClass::Find_Interval

### Curve1DClass::Find_Interval
- Purpose: Finds the interval containing a given time (supports looping)
- Calls: None

### LinearCurve1DClass::Evaluate
- Purpose: Evaluates the 1D curve at a given time
- Calls: Curve1DClass::Find_Interval

## Globals
- _LinearCurve3DFactory (SimplePersistFactoryClass): Factory for LinearCurve3DClass persistence
- _LinearCurve1DFactory (SimplePersistFactoryClass): Factory for LinearCurve1DClass persistence

## Dependencies
- curve.h (header)
- wwdebug.h (debug macros)
- persistfactory.h (persistence framework)
- wwmathids.h (chunk IDs)
- wwhack.h (assertions)
