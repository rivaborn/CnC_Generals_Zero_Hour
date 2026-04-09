# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vp.h

## Purpose
Header file defining the VectorProcessorClass, which provides optimized vector and matrix operations for the game engine.

## Responsibilities
- Declares vector and matrix transformation functions
- Provides data copying and manipulation utilities
- Exposes vector normalization, clamping, and mathematical operations
- Includes prefetching functionality for performance optimization

## Key Types
- Vector2 (Class): 2D vector type
- Vector3 (Class): 3D vector type
- Vector4 (Class): 4D vector type
- Matrix3D (Class): 3x3 matrix type
- Matrix4x4 (Class): 4x4 matrix type
- VectorProcessorClass (Class): Static class containing vector/matrix operations

## Key Functions
### VectorProcessorClass::Transform
- Purpose: Transforms vector arrays using matrices
- Calls: Not inferable

### VectorProcessorClass::Copy
- Purpose: Copies data between arrays of various types
- Calls: Not inferable

### VectorProcessorClass::CopyIndexed
- Purpose: Copies data with indexing for vertex manipulation
- Calls: Not inferable

### VectorProcessorClass::Normalize
- Purpose: Normalizes vector arrays
- Calls: Not inferable

### VectorProcessorClass::MinMax
- Purpose: Finds min/max values in vector arrays
- Calls: Not inferable

### VectorProcessorClass::DotProduct
- Purpose: Computes dot products between vectors
- Calls: Not inferable

## Globals
None

## Dependencies
- Key includes: None (header-only)
- External symbols: Vector2, Vector3, Vector4, Matrix3D, Matrix4x4 classes
