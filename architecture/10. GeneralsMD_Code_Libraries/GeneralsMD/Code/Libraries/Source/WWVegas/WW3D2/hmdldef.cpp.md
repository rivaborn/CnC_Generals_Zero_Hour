# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmdldef.cpp

## Purpose
Implements the HModelDefClass for loading and managing hierarchical model definitions in the W3D file format.

## Responsibilities
- Loads hierarchical model data from W3D files
- Manages sub-object connections and snap points
- Handles memory allocation/deallocation for model data
- Supports version compatibility for pre-3.0 W3D files

## Key Types
- HModelDefClass (Class): Main class for hierarchical model definitions
- HmdlNodeDefStruct (Struct): Represents a node connection in the hierarchy
- W3dHModelHeaderStruct (Struct): Header information for W3D hierarchical models
- W3dHModelNodeStruct (Struct): Node connection data structure

## Key Functions
### HModelDefClass::Load_W3D
- Purpose: Loads hierarchical model data from a W3D file chunk
- Calls: Free(), read_connection(), W3DNEWARRAY, W3DNEW

### HModelDefClass::read_connection
- Purpose: Reads a single node connection from the W3D file
- Calls: strcpy, strcat, assert

### HModelDefClass::Free
- Purpose: Deallocates all memory used by the model definition
- Calls: delete[]

## Globals
None

## Dependencies
- hmdldef.h (header)
- w3d_file.h (W3D file operations)
- chunkio.h (chunk loading)
- snappts.h (snap points)
- assert.h, string.h (standard libraries)
