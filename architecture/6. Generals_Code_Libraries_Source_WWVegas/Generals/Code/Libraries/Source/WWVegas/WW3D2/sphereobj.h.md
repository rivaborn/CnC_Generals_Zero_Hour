# Generals/Code/Libraries/Source/WWVegas/WW3D2/sphereobj.h

## Purpose
Defines classes for procedural sphere rendering in the W3D engine, including animation channels and loading infrastructure.

## Responsibilities
- Declares sphere mesh generation and rendering classes
- Defines animation channels for sphere properties (color, alpha, scale, vector)
- Provides loading/saving infrastructure for sphere prototypes
- Manages sphere-specific rendering flags and state

## Key Types
- **TextureClass (Class)**: Not inferable.
- **AlphaVectorStruct (Struct)**: Stores angle (quaternion) and intensity for alpha vector effects.
- **AlphaVectorChannel (Class)**: Animation channel for alpha vector properties with spherical interpolation.
- **W3dSphereStruct (Struct)**: File format structure for sphere definitions including keys and properties.
- **SphereFlags (Enum)**: Bitmask flags for sphere rendering features (alpha vector, camera alignment, etc.).
- **SphereMeshClass (Class)**: Handles mesh generation and vertex data for spheres.
- **SphereRenderObjClass (Class)**: Main renderable sphere object with animation and rendering logic.
- **SphereLoaderClass (Class)**: Prototype loader for sphere objects.
- **SpherePrototypeClass (Class)**: Prototype class for sphere objects with serialization support.

## Key Functions
### `SphereMeshClass::Generate`
- Purpose: Generates sphere mesh geometry with given radius and tessellation.
- Calls: Not inferable.

### `SphereRenderObjClass::Render`
- Purpose: Renders the sphere with current state and animation.
- Calls: `render_sphere`, `animate`.

### `SphereRenderObjClass::animate`
- Purpose: Updates sphere properties based on animation channels.
- Calls: Not inferable.

### `SpherePrototypeClass::Load`
- Purpose: Loads sphere definition from chunk data.
- Calls: Not inferable.

## Globals
- **_SphereLoader (SphereLoaderClass)**: Global instance of the sphere loader for asset management.

## Dependencies
- `rendobj.h`, `w3d_file.h`, `shader.h`, `proto.h`, `obbox.h`, `vector3i.h`, `quat.h`, `prim_anim.h`
- `RenderObjClass`, `PrototypeClass`, `PrototypeLoaderClass`, `ChunkLoadClass`, `ChunkSaveClass`, `Matrix3D`, `Vector3`, `Quaternion`, `AABoxClass`, `SphereClass`, `ShaderClass`, `TextureClass`, `PrimitiveAnimationChannelClass`, `LERPAnimationChannelClass`
