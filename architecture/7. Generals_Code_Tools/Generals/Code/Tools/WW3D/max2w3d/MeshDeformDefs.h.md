# Generals/Code/Tools/WW3D/max2w3d/MeshDeformDefs.h

## Purpose
Defines data structures and enums for mesh deformation operations in the 3DS Max to W3D exporter tool.

## Responsibilities
- Declares deformation channel flags (position/color)
- Defines vertex information structure (`VERT_INFO`)
- Provides a dynamic vector container for deformation lists (`DEFORM_LIST`)

## Key Types
- `DEFORM_CHANNELS` (Enum): flags for deformation channels (position/color)
- `VERT_INFO` (Struct): stores vertex index, color index, and 3D position/color value
- `DEFORM_LIST` (Class): dynamic vector of `VERT_INFO` objects

## Key Functions
### `_VERT_INFO/_VERT_INFO` (default constructor)
- Purpose: Initializes vertex info with default values
- Calls: None

### `_VERT_INFO/_VERT_INFO` (parameterized constructor)
- Purpose: Initializes vertex info with index, position, and optional color index
- Calls: None

### `_VERT_INFO/operator==`
- Purpose: Equality comparison (always returns false)
- Calls: None

### `_VERT_INFO/operator!=`
- Purpose: Inequality comparison (always returns true)
- Calls: None

## Globals
- None

## Dependencies
- `<Max.H>`: 3DS Max SDK headers
- `"Vector.H"`: Local vector math library
- `DynamicVectorClass`: Template container class from Max SDK
