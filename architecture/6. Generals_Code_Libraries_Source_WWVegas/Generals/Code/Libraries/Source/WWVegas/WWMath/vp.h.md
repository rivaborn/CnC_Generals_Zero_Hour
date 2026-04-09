# Generals/Code/Libraries/Source/WWVegas/WWMath/vp.h

## Purpose
Header file declaring the VectorProcessorClass, which provides optimized vector math operations for the game engine.

## Responsibilities
- Declares vector and matrix transformation functions
- Provides bulk vector operations (copy, clamp, normalize)
- Exposes SIMD-optimized math utilities
- Supports indexed data access patterns

## Key Types
- Vector2 (Class): 2D vector type
- Vector3 (Class): 3D vector type
- Vector4 (Class): 4D vector type
- Matrix3D (Class): 3x3 transformation matrix
- Matrix4 (Class): 4x4 transformation matrix
- VectorProcessorClass (Class): Static class for vector operations

## Key Functions
### VectorProcessorClass::Transform
- Purpose: Transforms vector arrays using matrices
- Calls: Not inferable

### VectorProcessorClass::Copy
- Purpose: Copies vector/memory blocks
- Calls: Not inferable

### VectorProcessorClass::CopyIndexed
- Purpose: Copies data using index arrays
- Calls: Not inferable

### VectorProcessorClass::Normalize
- Purpose: Normalizes vector arrays
- Calls: Not inferable

### VectorProcessorClass::MinMax
- Purpose: Finds min/max vectors in an array
- Calls: Not inferable

## Globals
None

## Dependencies
- Key includes: None (header-only)
- External symbols: Vector2, Vector3, Vector4, Matrix3D, Matrix4 (forward declarations)
