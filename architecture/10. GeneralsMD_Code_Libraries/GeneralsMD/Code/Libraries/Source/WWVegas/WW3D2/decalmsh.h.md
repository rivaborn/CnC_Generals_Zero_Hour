# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.h

## Purpose
Header file defining decal mesh classes for the W3D rendering system, supporting dynamic decals on 3D meshes.

## Responsibilities
- Declares abstract `DecalMeshClass` and concrete implementations (`RigidDecalMeshClass`, `SkinDecalMeshClass`)
- Defines decal creation/deletion and rendering interfaces
- Manages decal organization via `DecalStruct` and material handling

## Key Types
- **DecalMeshClass (Class)**: Abstract base class for decal meshes
- **RigidDecalMeshClass (Class)**: Decal mesh for rigid (static) geometry
- **SkinDecalMeshClass (Class)**: Decal mesh for skinned (dynamic) geometry
- **DecalStruct (Struct)**: Stores decal metadata (ID, vertex/face ranges)

## Key Functions
### `Create_Decal`
- Purpose: Creates a new decal on the mesh
- Calls: Not inferable (pure virtual)

### `Delete_Decal`
- Purpose: Removes a decal by its ID
- Calls: Not inferable (pure virtual)

### `Render`
- Purpose: Renders all decals on the mesh
- Calls: Not inferable (pure virtual)

## Globals
None

## Dependencies
- Key includes: `always.h`, `vector.h`, `shader.h`, `meshgeometry.h`
- External symbols: `MeshClass`, `DecalSystemClass`, `DecalGeneratorClass`, `OBBoxClass`, `TextureClass`
