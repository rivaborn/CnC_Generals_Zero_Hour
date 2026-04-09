# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmorphanim.cpp - Enhanced Analysis

## Architectural Role
This file implements the morph animation system for the W3D (Westwood 3D) model format, enabling blend animations between hierarchical pose states. It bridges the asset pipeline (loading/saving) with runtime interpolation, supporting the engine's skeletal animation hierarchy.

## Cross-References
### Incoming
- **Animation System**: Likely called by animation controllers (e.g., `hierarchy.cpp`) to evaluate morph targets.
- **Asset Pipeline**: Used by asset loaders (e.g., `w3d_file.cpp`) during model initialization.
- **UI/Editor Tools**: Potentially referenced by animation editors for morph key manipulation.

### Outgoing
- **Asset Management**: Relies on `WW3DAssetManager` for hierarchical animation (HAnim) references.
- **Math Utilities**: Uses `Vector3`, `Quaternion`, and `Matrix3D` for interpolation and transform math.
- **File I/O**: Depends on `ChunkLoadClass`/`ChunkSaveClass` for binary serialization.

## Design Patterns
- **Resource Pooling**: `WW3DAssetManager` singleton manages HAnim references, avoiding duplication.
- **Lazy Evaluation**: `get_index` caches the last searched key to optimize sequential frame queries.
- **Strategy Pattern**: Morph interpolation (lerp/slerp) is abstracted for reuse across translation/orientation.
