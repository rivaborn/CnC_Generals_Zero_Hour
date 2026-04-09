# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/catmullromspline.cpp

## Purpose
Implements Catmull-Rom spline classes for 1D and 3D interpolation, including tangent calculation and persistence.

## Responsibilities
- Computes tangents for spline keys
- Provides persistence (save/load) for spline data
- Manages looping vs. non-looping spline behavior
- Exposes factory methods for serialization

## Key Types
- (anonymous enum) (Enum): Chunk IDs for persistence
- CATMULLROM3D_CHUNK_HERMITE3D (Enum): 3D spline chunk ID
- CATMULLROM1D_CHUNK_HERMITE1D (Enum): 1D spline chunk ID

## Key Functions
### CatmullRomSpline3DClass::Update_Tangents
- Purpose: Computes tangents at each key point for 3D spline
- Calls: None directly visible

### CatmullRomSpline3DClass::Get_Factory
- Purpose: Returns persistence factory for 3D spline
- Calls: None

### CatmullRomSpline3DClass::Save
- Purpose: Saves 3D spline data to chunk stream
- Calls: HermiteSpline3DClass::Save

### CatmullRomSpline3DClass::Load
- Purpose: Loads 3D spline data from chunk stream
- Calls: HermiteSpline3DClass::Load, WWDEBUG_SAY

### CatmullRomSpline1DClass::Update_Tangents
- Purpose: Computes tangents at each key point for 1D spline
- Calls: None directly visible

### CatmullRomSpline1DClass::Get_Factory
- Purpose: Returns persistence factory for 1D spline
- Calls: None

### CatmullRomSpline1DClass::Save
- Purpose: Saves 1D spline data to chunk stream
- Calls: HermiteSpline1DClass::Save

### CatmullRomSpline1DClass::Load
- Purpose: Loads 1D spline data from chunk stream
- Calls: HermiteSpline1DClass::Load, WWDEBUG_SAY

## Globals
- _CatmullRomSpline3DFactory (SimplePersistFactoryClass): Factory for 3D spline persistence
- _CatmullRomSpline1DFactory (SimplePersistFactoryClass): Factory for 1D spline persistence

## Dependencies
- catmullromspline.h
- persistfactory.h
- wwmathids.h
- wwhack.h
