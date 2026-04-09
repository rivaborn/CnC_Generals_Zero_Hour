# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalmsh.h

## Purpose
Header file defining decal mesh classes for rendering decals on 3D meshes in the SAGE engine.

## Responsibilities
- Declares abstract `DecalMeshClass` and concrete implementations (`RigidDecalMeshClass`, `SkinDecalMeshClass`)
- Defines decal management interfaces (creation, deletion, rendering)
- Handles both static (rigid) and dynamic (skin) mesh decals

## Key Types
- **DecalMeshClass (Class)**: Abstract base class for decal meshes.
- **RigidDecalMeshClass (Class)**: Concrete class for decals on static meshes.
- **SkinDecalMeshClass (Class)**: Concrete class for decals on skinned meshes.
- **DecalStruct (Struct)**: Stores decal metadata (ID, vertex/face indices).
- **MeshClass (Class)**: Parent mesh reference (forward declaration).
- **DecalSystemClass (Class)**: Decal management system (forward declaration).

## Key Functions
### DecalMeshClass::Create_Decal
- Purpose: Creates a new decal on the mesh.
- Calls: Not visible in header.

### RigidDecalMeshClass::Render
- Purpose: Renders all decals in the rigid mesh.
- Calls: Not visible in header.

### SkinDecalMeshClass::Render
- Purpose: Renders all decals in the skinned mesh.
- Calls: Not visible in header.

## Globals
None.

## Dependencies
- Key includes: `always.h`, `bittype.h`, `simplevec.h`, `vector.h`, `shader.h`, `vertmaterial.h`
- External symbols: `MeshClass`, `DecalSystemClass`, `DecalGeneratorClass`, `OBBoxClass`, `TextureClass`
