# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/sphereobj.h

## Purpose
Defines classes for procedural sphere rendering in the W3D engine, including animation channels, mesh generation, and prototype loading.

## Responsibilities
- Procedural sphere mesh generation and rendering
- Animation channel management for color, alpha, scale, and vector properties
- LOD (Level of Detail) handling for spheres
- Prototype loading/saving for sphere objects

## Key Types
- **TextureClass (Class)**: Not defined here; used for texture references.
- **AlphaVectorStruct (Struct)**: Stores angle (quaternion) and intensity for alpha vector effects.
- **AlphaVectorChannel (Class)**: Animation channel for alpha vector properties with spherical interpolation.
- **W3dSphereStruct (Struct)**: File format structure for sphere definitions.
- **SphereMeshClass (Class)**: Manages vertex data and rendering strips/fans for sphere meshes.
- **SphereRenderObjClass (Class)**: Main render object class for spheres with animation and LOD support.
- **SphereFlags (Enum)**: Bit flags for sphere rendering options (alpha vector, camera alignment, etc.).
- **SphereLoaderClass (Class)**: Prototype loader for sphere objects.
- **SpherePrototypeClass (Class)**: Prototype class for sphere objects with load/save functionality.

## Key Functions
### `SphereMeshClass::Generate`
- Purpose: Generates sphere mesh geometry with given radius, slices, and stacks.
- Calls: Not inferable from header.

### `SphereRenderObjClass::Render`
- Purpose: Renders the sphere with current state and animation.
- Calls: `render_sphere`, `animate`.

### `SphereRenderObjClass::animate`
- Purpose: Updates animation state based on current time.
- Calls: Animation channel evaluation methods.

### `SpherePrototypeClass::Load`
- Purpose: Loads sphere definition from a chunk load stream.
- Calls: `ChunkLoadClass` methods.

## Globals
- **_SphereLoader (SphereLoaderClass)**: Global instance of the sphere loader for asset management.

## Dependencies
- Key includes: `rendobj.h`, `w3d_file.h`, `shader.h`, `proto.h`, `obbox.h`, `vector3i.h`, `quat.h`, `prim_anim.h`, `meshgeometry.h`
- External symbols: `RenderObjClass`, `TextureClass`, `ShaderClass`, `PrototypeClass`, `ChunkLoadClass`, `ChunkSaveClass`, `Matrix3D`, `Vector3`, `Quaternion`, `AABoxClass`, `SphereClass`
