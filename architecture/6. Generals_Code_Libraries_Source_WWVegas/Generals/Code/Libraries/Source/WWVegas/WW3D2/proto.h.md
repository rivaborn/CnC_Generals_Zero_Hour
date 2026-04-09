# Generals/Code/Libraries/Source/WWVegas/WW3D2/proto.h

## Purpose
Defines the prototype system for W3D render objects, including prototype loaders and concrete implementations for meshes and hierarchical models.

## Responsibilities
- Declares abstract base classes for prototypes and prototype loaders
- Defines concrete prototype loaders for mesh and HModel chunks
- Provides global instances of default loaders for automatic asset manager installation

## Key Types
- **PrototypeClass (Class)**: Abstract base class for render object prototypes.
- **PrimitivePrototypeClass (Class)**: Concrete prototype implementation for primitive render objects.
- **PrototypeLoaderClass (Class)**: Abstract base class for prototype loaders.
- **MeshLoaderClass (Class)**: Concrete loader for W3D mesh chunks.
- **HModelLoaderClass (Class)**: Concrete loader for W3D hierarchical model chunks.

## Key Functions
### PrototypeClass::Create
- Purpose: Creates a new render object instance from the prototype.
- Calls: Not inferable (pure virtual).

### PrototypeLoaderClass::Load_W3D
- Purpose: Loads a prototype from a W3D chunk.
- Calls: Not inferable (pure virtual).

### MeshLoaderClass::Load_W3D
- Purpose: Loads a mesh prototype from a W3D mesh chunk.
- Calls: Not inferable.

### HModelLoaderClass::Load_W3D
- Purpose: Loads an HModel prototype from a W3D hierarchical model chunk.
- Calls: Not inferable.

## Globals
- **_MeshLoader (MeshLoaderClass)**: Global instance of the mesh loader.
- **_HModelLoader (HModelLoaderClass)**: Global instance of the HModel loader.

## Dependencies
- `always.h`, `w3d_file.h`
- `RenderObjClass`, `ChunkLoadClass`, `W
