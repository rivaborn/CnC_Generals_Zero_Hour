# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/nullrobj.h

## Purpose
Defines classes for handling null 3D objects in the W3D rendering system.

## Responsibilities
- Defines `Null3DObjClass` for rendering null objects
- Provides `NullPrototypeClass` for prototype management
- Implements `NullLoaderClass` for loading null objects from W3D files
- Declares global loader instance `_NullLoader`

## Key Types
- **Null3DObjClass (Class)**: Represents a null 3D object with basic rendering capabilities
- **NullPrototypeClass (Class)**: Prototype class for null objects with memory pool management
- **NullLoaderClass (Class)**: Loader for W3D null object chunks

## Key Functions
### Null3DObjClass::Render
- Purpose: Renders the null object (likely does nothing)
- Calls: Not inferable

### NullPrototypeClass::Create
- Purpose: Creates a new Null3DObjClass instance
- Calls: NEW_REF

### NullLoaderClass::Load_W3D
- Purpose: Loads null object data from W3D chunk
- Calls: Not inferable

## Globals
- **_NullLoader (NullLoaderClass)**: Global loader instance for automatic asset manager installation

## Dependencies
- `rendobj.h` (RenderObjClass)
- `proto.h` (PrototypeClass, W3DMPO)
- W3D chunk system (W3D_CHUNK_NULL_OBJECT)
- Memory pool system (W3DMPO_GLUE)
