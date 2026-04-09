# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/proto.h

## Purpose
Defines the W3D prototype system for render object creation, including prototype loaders and default loaders for meshes and HModels.

## Responsibilities
- Declares abstract base classes for prototypes and prototype loaders
- Defines concrete prototype loaders for W3D mesh and HModel chunks
- Provides global instances of default loaders for automatic asset manager installation

## Key Types
- **PrototypeClass (Class)**: Abstract base class for render object prototypes
- **PrimitivePrototypeClass (Class)**: Concrete prototype for simple render objects via cloning
- **PrototypeLoaderClass (Class)**: Abstract base class for W3D chunk loaders
- **MeshLoaderClass (Class)**: Loader for W3D mesh chunks
- **HModelLoaderClass (Class)**: Loader for W3D HModel chunks

## Key Functions
### PrototypeClass::Create
- Purpose: Creates a new render object instance
- Calls: Not inferable

### PrototypeLoaderClass::Load_W3D
- Purpose: Loads a prototype from a W3D chunk
- Calls: Not inferable

### MeshLoaderClass::Load_W3D
- Purpose: Loads a mesh prototype from a W3D mesh chunk
- Calls: Not inferable

### HModelLoaderClass::Load_W3D
- Purpose: Loads an HModel prototype from a W3D HModel chunk
- Calls: Not inferable

## Globals
- **_MeshLoader (MeshLoaderClass)**: Global instance of mesh loader
- **_HModelLoader (HModelLoaderClass)**: Global instance of HModel loader

## Dependencies
- `always.h`, `w3d_file.h`
- `RenderObjClass`, `ChunkLoadClass`, `W3DMP
