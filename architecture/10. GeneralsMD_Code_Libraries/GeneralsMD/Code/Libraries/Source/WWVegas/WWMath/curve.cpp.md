# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/curve.cpp

## Purpose
Implements 1D and 3D curve classes for interpolation, including linear curves and persistence support.

## Responsibilities
- Manages key-based interpolation for 1D and 3D curves
- Handles curve persistence (save/load)
- Provides linear interpolation implementations
- Supports looping curves
- Manages curve key manipulation (add/remove/modify)

## Key Types
- Curve3DClass (Class): Base class for 3D curves with key management
- LinearCurve3DClass (Class): Linear interpolation for 3D curves
- Curve1DClass (Class): Base class for 1D curves with key management
- LinearCurve1DClass (Class): Linear interpolation for 1D curves
- (anonymous enum) (Enum): Chunk ID definitions for persistence

## Key Functions
### Curve3DClass::Find_Interval
- Purpose: Finds the interval containing a given time
- Calls: None

### LinearCurve3DClass::Evaluate
- Purpose: Evaluates the curve at a given time using linear interpolation
- Calls: Curve3DClass::Find_Interval

### Curve1DClass::Find_Interval
- Purpose: Finds the interval containing a given time (supports looping)
- Calls: None

### LinearCurve1DClass::Evaluate
- Purpose: Evaluates the curve at a given time using linear interpolation
- Calls: Curve1DClass::Find_Interval

## Globals
- _LinearCurve3DFactory (SimplePersistFactoryClass): Persistence factory for LinearCurve3DClass
- _LinearCurve1DFactory (SimplePersistFactoryClass): Persistence factory for LinearCurve1DClass

## Dependencies
- curve.h
- wwdebug.h
- persistfactory.h
- wwmathids.h
- wwhack.h
- ChunkSaveClass, ChunkLoadClass (external)
- Vector3 (external)
- SimplePersistFactoryClass (external)
