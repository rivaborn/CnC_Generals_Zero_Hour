# Generals/Code/Libraries/Source/WWVegas/WWMath/vp.cpp

## Purpose
Implements vector and matrix operations optimized for SSE instructions, providing fast transformations and data manipulation.

## Responsibilities
- Optimized vector/matrix transformations using SSE
- Memory copy and indexed copy operations
- Vector normalization, clamping, and min/max calculations
- Dot product and scalar operations

## Key Types
- VectorProcessorClass (Class): Provides optimized vector/matrix operations
- Vector2/Vector3/Vector4 (Structs): Vector types used throughout
- Matrix3D/Matrix4 (Classes): Matrix types for transformations

## Key Functions
### Transform(Vector3* dst, const Vector3 *src, const Matrix3D& mtx, int count)
- Purpose: Transforms array of Vector3 using Matrix3D with SSE optimization
- Calls: Matrix3D::mulVector3Array (fallback), memcpy, SSE intrinsics

### Transform(Vector4* dst, const Vector3 *src, const Matrix4& matrix, int count)
- Purpose: Transforms array of Vector3 to Vector4 using Matrix4
- Calls: Matrix4 operator*, memcpy

### Copy methods
- Purpose: Various optimized copy operations for different vector types
- Calls: memcpy

### Clamp/Normalize/MinMax/DotProduct/Power
- Purpose: Vector math operations applied to arrays
- Calls: None (direct math operations)

## Globals
- lastrow (Vector4): Default last row for matrix transformations (0,0,0,1)

## Dependencies
- vector2.h, vector3.h, vector4.h, matrix3d.h, matrix4.h
- cpudetect.h (for SSE detection)
- wwdebug.h
- <memory.h>
