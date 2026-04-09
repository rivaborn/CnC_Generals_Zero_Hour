# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vp.cpp

## Purpose
Implements vector and matrix operations optimized for SSE instructions, providing fast transformations and data manipulation for 3D graphics.

## Responsibilities
- Optimized vector/matrix transformations using SSE
- Memory copy and indexed copy operations
- Vector normalization, clamping, and min/max calculations
- Dot product and scalar operations

## Key Types
- VectorProcessorClass (Class): Provides optimized vector/matrix operations
- Vector2/Vector3/Vector4 (Structs): Vector types used throughout
- Matrix3D/Matrix4x4 (Classes): Matrix types for transformations

## Key Functions
### Transform(Vector3*, const Vector3*, const Matrix3D&, int)
- Purpose: Transforms array of Vector3 using Matrix3D with SSE optimization
- Calls: Matrix3D::mulVector3Array (fallback), memcpy

### Transform(Vector4*, const Vector3*, const Matrix4x4&, int)
- Purpose: Transforms array of Vector3 to Vector4 using Matrix4x4
- Calls: Matrix4x4::operator* (implicit)

### Copy(Vector4*, const Vector3*, const float*, int)
- Purpose: Copies Vector3 to Vector4 with per-element W component
- Calls: None

### Clamp(Vector4*, const Vector4*, float, float, int)
- Purpose: Clamps vector components between min/max values
- Calls: None

### Normalize(Vector3*, int)
- Purpose: Normalizes array of Vector3
- Calls: Vector3::Normalize

## Globals
- lastrow (Vector4): Default last row for matrix transformations (0,0,0,1)

## Dependencies
- vector2.h, vector3.h, vector4.h, matrix3d.h, matrix4.h
- wwdebug.h, cpudetect.h
- Uses inline assembly for SSE instructions
- Uses memcpy from memory.h
