# Generals/Code/Libraries/Source/WWVegas/WWMath/cardinalspline.cpp

## Purpose
Implements 1D and 3D cardinal spline classes for interpolation, including persistence and tangent calculation.

## Responsibilities
- Manages key points and tangents for spline interpolation
- Handles tightness parameters for controlling spline smoothness
- Implements persistence (save/load) for spline data
- Updates tangents based on key positions and tightness
- Provides factory registration for persistence system

## Key Types
- (anonymous enum) (Enum): Chunk IDs for persistence
- CARDINAL3D_CHUNK_HERMITE3D (Enum): Chunk ID for 3D Hermite data
- CARDINAL3D_CHUNK_TIGHTNESSKEYS (Enum): Chunk ID for 3D tightness keys
- CARDINAL1D_CHUNK_HERMITE1D (Enum): Chunk ID for 1D Hermite data
- CARDINAL1D_CHUNK_TIGHTNESSKEYS (Enum): Chunk ID for 1D tightness keys

## Key Functions
### CardinalSpline3DClass::Update_Tangents
- Purpose: Calculates tangents for 3D spline based on key positions and tightness
- Calls: None

### CardinalSpline3DClass::Save
- Purpose: Saves spline data to chunk stream
- Calls: HermiteSpline3DClass::Save

### CardinalSpline3DClass::Load
- Purpose: Loads spline data from chunk stream
- Calls: HermiteSpline3DClass::Load

### CardinalSpline1DClass::Update_Tangents
- Purpose: Calculates tangents for 1D spline based on key positions and tightness
- Calls: None

### CardinalSpline1DClass::Save
- Purpose: Saves 1D spline data to chunk stream
- Calls: HermiteSpline1DClass::Save

### CardinalSpline1DClass::Load
- Purpose: Loads 1D spline data from chunk stream
- Calls: HermiteSpline1DClass::Load

## Globals
- _CardinalSpline3DFactory (SimplePersistFactoryClass): Factory for 3D spline persistence
- _CardinalSpline1DFactory (SimplePersistFactoryClass): Factory for 1D spline persistence

## Dependencies
- cardinalspline.h
- wwdebug.h
- persistfactory.h
- wwmathids.h
- wwhack.h
- ChunkSaveClass
- ChunkLoadClass
- HermiteSpline3DClass
- HermiteSpline1
