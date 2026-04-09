# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/catmullromspline.h

## Purpose
Defines Catmull-Rom spline classes for 3D and 1D interpolation, inheriting from Hermite splines.

## Responsibilities
- Provides 3D and 1D Catmull-Rom spline implementations
- Manages tangent updates for spline interpolation
- Supports serialization via Save/Load methods
- Inherits core functionality from HermiteSpline classes

## Key Types
- **CatmullRomSpline3DClass (Class)**: 3D Catmull-Rom spline implementation
- **CatmullRomSpline1DClass (Class)**: 1D Catmull-Rom spline implementation

## Key Functions
### CatmullRomSpline3DClass::Update_Tangents
- Purpose: Updates tangents for 3D spline interpolation
- Calls: Not inferable

### CatmullRomSpline3DClass::Get_Factory
- Purpose: Returns persistence factory for serialization
- Calls: Not inferable

### CatmullRomSpline3DClass::Save
- Purpose: Serializes spline data
- Calls: ChunkSaveClass methods

### CatmullRomSpline3DClass::Load
- Purpose: Deserializes spline data
- Calls: ChunkLoadClass methods

### CatmullRomSpline1DClass::Update_Tangents
- Purpose: Updates tangents for 1D spline interpolation
- Calls: Not inferable

### CatmullRomSpline1DClass::Get_Factory
- Purpose: Returns persistence factory for serialization
- Calls: Not inferable

### CatmullRomSpline1DClass::Save
- Purpose: Serializes spline data
