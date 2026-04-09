# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshmdl.h

## Purpose
Header file defining the `MeshModelClass` and related classes for 3D mesh rendering in the SAGE engine.

## Responsibilities
- Declares mesh model classes and their interfaces
- Defines geometry, material, and rendering data structures
- Provides loading/saving and rendering support for 3D meshes

## Key Types
- **MeshModelClass (Class)**: Main mesh model container with geometry and material data
- **GapFillerClass (Class)**: Handles gap filling between polygons
- **VertexFormatXYZNDUV2 (Struct)**: Vertex format with position, normal, and UV coordinates
- **TextureClass (Class)**: Texture reference
- **RenderInfoClass (Class)**: Rendering information
- **MaterialInfoClass (Class)**: Material information container

## Key Functions
### `Load_W3D`
- Purpose: Loads a W3D mesh file format
- Calls: `read_chunks`, `read_texcoords`, `read_materials`, etc.

### `Register_For_Rendering`
- Purpose: Registers the mesh model for rendering
- Calls: Not inferable

### `Shadow_Render`
- Purpose: Renders the mesh as a shadow
- Calls: Not inferable

## Globals
- None

## Dependencies
- Key includes: `vector2.h`, `vector3.h`, `vector4.h`, `vector3i.h`, `sharebuf.h`, `shader.h`, `wwdebug.h`, `vertmaterial.h`, `bittype.h`, `colmath.h`, `simplevec.h`, `wwstring.h`, `rinfo.h`, `meshgeometry.h`, `meshmatdesc.h`, `dx8list.h`
- External symbols: `W3DMPO`, `WW3DErrorType`, `Matrix3D`, `HTreeClass`, `DecalGeneratorClass`, `MeshClass`, `DX8FVFCategoryContainer`, `VertexMaterialClass`, `TextureClass`, `ShaderClass`
