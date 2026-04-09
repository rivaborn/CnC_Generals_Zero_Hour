# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/proto.cpp

## Purpose
Implements prototype classes and loaders for W3D mesh and HModel assets.

## Responsibilities
- Defines `PrimitivePrototypeClass` and `HModelPrototypeClass` for asset prototyping
- Implements `MeshLoaderClass` and `HModelLoaderClass` for loading W3D assets
- Manages reference counting for loaded assets
- Handles error cases during asset loading

## Key Types
- **PrimitivePrototypeClass (Class)**: Wraps a `RenderObjClass` prototype for primitive assets
- **HModelPrototypeClass (Class)**: Prototype for hierarchical models (`HModelDefClass`)
- **MeshLoaderClass (Class)**: Loads mesh assets and creates prototypes
- **HModelLoaderClass (Class)**: Loads HModel definitions and creates prototypes

## Key Functions
### MeshLoaderClass::Load_W3D
- Purpose: Loads a W3D mesh and creates a prototype
- Calls: `MeshClass::Load_W3D`, `PrimitivePrototypeClass` constructor

### HModelLoaderClass::Load_W3D
- Purpose: Loads an HModel definition and creates a prototype
- Calls: `HModelDefClass::Load_W3D`, `HModelPrototypeClass` constructor

## Globals
- **_MeshLoader (MeshLoaderClass)**: Default mesh loader instance
- **_HModelLoader (HModelLoaderClass)**: Default HModel loader instance

## Dependencies
- `proto.h`, `mesh.h`, `hmdldef.h`, `hlod.h`, `w3derr.h`
- `RenderObjClass`, `ChunkLoadClass`, `MeshClass`, `HModelDefClass`, `HLodClass`
