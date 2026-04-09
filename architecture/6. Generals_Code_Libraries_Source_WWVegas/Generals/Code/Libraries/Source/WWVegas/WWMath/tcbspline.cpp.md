# Generals/Code/Libraries/Source/WWVegas/WWMath/tcbspline.cpp

## Purpose
Implements TCB (Tension, Continuity, Bias) spline functionality for 3D curves, extending Hermite splines with TCB parameters.

## Responsibilities
- Manages TCB spline keys, tangents, and parameters
- Handles saving/loading spline data via chunk system
- Computes tangents based on TCB parameters
- Supports looping and non-looping splines

## Key Types
- TCBClass (Struct): Stores tension, continuity, and bias parameters
- TCBSpline3DClass (Class): Main spline class managing keys, tangents, and TCB parameters
- (anonymous enum) (Enum): Defines chunk IDs for save/load system

## Key Functions
### Add_Key
- Purpose: Adds a new key to the spline with default TCB parameters
- Calls: HermiteSpline3DClass::Add_Key, Params.Insert

### Update_Tangents
- Purpose: Recalculates tangents based on current TCB parameters
- Calls: Vector3::Subtract, Vector3::Add, Vector3::operator*

### Save/Load
- Purpose: Serializes/deserializes spline data using chunk system
- Calls: HermiteSpline3DClass::Save/Load, ChunkSaveClass/ChunkLoadClass methods

## Globals
- _TCBSpline3DFactory (SimplePersistFactoryClass): Factory for TCBSpline3DClass persistence

## Dependencies
- tcbspline.h, wwdebug.h, persistfactory.h, wwmathids.h, wwhack.h
- HermiteSpline3DClass, Vector3, ChunkSaveClass, ChunkLoadClass
