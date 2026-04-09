# Generals/Code/Libraries/Source/WWVegas/WWMath/curve.h

## Purpose
Defines curve classes for 1D and 3D interpolation, supporting key points and persistence.

## Responsibilities
- Provides base classes for 1D and 3D curves
- Supports key point management and evaluation
- Implements persistence via ChunkLoad/ChunkSave
- Includes linear interpolation implementations

## Key Types
- **Curve3DClass (Class)**: Base class for 3D curves with key points
- **KeyClass (Struct)**: Stores point and time for 3D keys
- **LinearCurve3DClass (Class)**: Linear interpolation 3D curve
- **Curve1DClass (Class)**: Base class for 1D curves
- **KeyClass (Struct)**: Stores point, time, and extra data for 1D keys
- **LinearCurve1DClass (Class)**: Linear interpolation 1D curve

## Key Functions
### Curve3DClass::Evaluate
- Purpose: Evaluates curve at given time
- Calls: Find_Interval

### Curve3DClass::Find_Interval
- Purpose: Finds interval containing given time
- Calls: None

### LinearCurve3DClass::Evaluate
- Purpose: Linearly interpolates between key points
- Calls: Curve3DClass::Find_Interval

### Curve1DClass::Evaluate
- Purpose: Evaluates 1D curve at given time
- Calls: Find_Interval

### LinearCurve1DClass::Evaluate
- Purpose: Linearly interpolates 1D key points
- Calls: Curve1DClass::Find_Interval

## Globals
- None

## Dependencies
- `always.h`, `vector.h`, `vector3.h`, `persist.h`
- `ChunkLoadClass`, `ChunkSaveClass
