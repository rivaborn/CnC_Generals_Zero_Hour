# Generals/Code/Tools/WW3D/max2w3d/hlodsave.h

## Purpose
Defines the HLodSaveClass for exporting hierarchical LOD (Level of Detail) models from 3D mesh connections.

## Responsibilities
- Manages LOD model export process
- Handles header and array data serialization
- Allocates and manages sub-object structures
- Integrates with 3DS Max SDK for node processing

## Key Types
- **HLodSaveClass (Class)**: Main class for LOD model export
- **HLodArrayEntry (Class)**: Holds LOD tree data for serialization
- **INodeListClass (Class)**: External node list interface
- **MeshConnectionsClass (Class)**: External mesh connection interface

## Key Functions
### HLodSaveClass::Save
- Purpose: Main export function for LOD model
- Calls: save_header, save_lod_arrays, save_aggregate_array, save_proxy_array

### HLodArrayEntry::Allocate_Sub_Objects
- Purpose: Allocates memory for sub-object array
- Calls: None

### save_header
- Purpose: Serializes LOD header data
- Calls: Not inferable

### save_lod_arrays
- Purpose: Serializes LOD array data
- Calls: Not inferable

### save_aggregate_array
- Purpose: Serializes aggregate array data
- Calls: Not inferable

### save_proxy_array
- Purpose: Serializes proxy array data
- Calls: Not inferable

### save_sub_object_array
- Purpose: Serializes sub-object array data
- Calls: Not inferable

## Globals
None

## Dependencies
- `always.h`, `<Max.h>`, `<stdio.h>`
- `w3d_file.h`, `progress.h`, `chunkio.h`, `meshcon.h`
-
