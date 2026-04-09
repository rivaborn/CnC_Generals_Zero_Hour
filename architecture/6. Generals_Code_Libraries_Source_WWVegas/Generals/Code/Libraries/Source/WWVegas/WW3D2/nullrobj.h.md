# Generals/Code/Libraries/Source/WWVegas/WW3D2/nullrobj.h

## Purpose
Defines classes for handling null 3D objects in the W3D rendering system.

## Responsibilities
- Provides a null 3D object class for placeholder rendering
- Implements prototype and loader classes for null objects
- Defines memory management and chunk loading for null objects

## Key Types
- **Null3DObjClass (Class)**: Represents a null 3D object with basic rendering capabilities
- **NullPrototypeClass (Class)**: Prototype class for creating null 3D objects
- **NullLoaderClass (Class)**: Loader for null object chunks in W3D files

## Key Functions
### Null3DObjClass::Render
- Purpose: Renders the null object (likely does nothing)
- Calls: Not inferable

### NullPrototypeClass::Create
- Purpose: Creates a new Null3DObjClass instance
- Calls: NEW_REF

### NullLoaderClass::Load_W3D
- Purpose: Loads null object data from a W3D chunk
- Calls: Not inferable

## Globals
- **_NullLoader (NullLoaderClass)**: Default loader instance for null objects

## Dependencies
- "rendobj.h" (RenderObjClass)
- "proto.h" (PrototypeClass, W3DMPO)
- W3D_CHUNK_NULL_OBJECT constant
- W3dNullObjectStruct
- W3D_NAME_LEN constant
