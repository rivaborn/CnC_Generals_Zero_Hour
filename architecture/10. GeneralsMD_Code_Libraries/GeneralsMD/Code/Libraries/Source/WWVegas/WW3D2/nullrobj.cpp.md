# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/nullrobj.cpp

## Purpose
Implements a null 3D object loader and prototype for the WW3D2 engine, providing a placeholder object type.

## Responsibilities
- Defines `Null3DObjClass` for rendering null objects
- Implements `NullPrototypeClass` for null object prototypes
- Provides `NullLoaderClass` to load null objects from chunks
- Handles object cloning and bounding calculations

## Key Types
- `Null3DObjClass` (Class): Represents a null 3D object with minimal rendering
- `NullPrototypeClass` (Class): Prototype for null objects with W3D definition
- `NullLoaderClass` (Class): Loader for null objects from chunk data

## Key Functions
### `Null3DObjClass::Render`
- Purpose: Empty render function for null objects
- Calls: None

### `NullLoaderClass::Load_W3D`
- Purpose: Loads null object data from chunk stream
- Calls: `cload.Read`, `W3DNEW NullPrototypeClass`

## Globals
- `_NullLoader` (NullLoaderClass): Global instance of the null object loader

## Dependencies
- `nullrobj.h`, `chunkio.h`
- `RenderObjClass`, `SphereClass`, `AABoxClass`, `PrototypeClass`
- `NEW_REF`, `W3DNEW` macros
