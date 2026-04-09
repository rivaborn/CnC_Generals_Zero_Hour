# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/projector.h - Enhanced Analysis

## Architectural Role
This file defines the core projection abstraction in the SAGE engine's 3D rendering pipeline, serving as a base class for texture projection and decal systems. It bridges the transformation system (Matrix3D/Matrix4x4) with spatial queries (bounding volumes) and texture mapping (MatrixMapperClass).

## Cross-References
### Incoming
- **Rendering Pipeline**: Likely called by shader/material systems for texture coordinate generation
- **Decal System**: Used by decal generators for projection calculations
- **Lighting System**: May be referenced for projective lighting effects

### Outgoing
- **Math Library**: Uses Matrix3D, Matrix4x4, and bounding volume classes
- **Texture System**: Interfaces with MatrixMapperClass for texture coordinate mapping

## Design Patterns
- **Template Method**: `Update_WS_Bounding_Volume()` is virtual, allowing subclasses to customize bounding volume updates
- **Composite**: Acts as a base class for projection hierarchies (TexProjectClass, DecalGeneratorClass)
- **Data Transfer Object**: Encapsulates projection parameters (matrices, volumes) for transfer between systems

*Not inferable*: Exact relationship with MatrixMapperClass implementation details.
