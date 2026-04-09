# Generals/Code/Tools/WW3D/max2w3d/hlodsave.cpp

## Purpose
Handles saving Hierarchical Level of Detail (HLOD) data to W3D files for the game engine.

## Responsibilities
- Constructs HLOD tree structure for saving
- Writes HLOD header, LOD arrays, aggregates, and proxies
- Manages chunk-based W3D file writing
- Handles mesh-to-bone connectivity data

## Key Types
- **HLodSaveClass (Class)**: Main class for HLOD saving functionality
- **W3dHLodHeaderStruct (Struct)**: Contains HLOD version, LOD count, and names
- **W3dHLodArrayHeaderStruct (Struct)**: Stores model count and screen size
- **W3dHLodSubObjectStruct (Struct)**: Holds bone index and mesh name
- **HLodArrayEntry (Struct)**: Represents an LOD array entry

## Key Functions
### HLodSaveClass::Save
- Purpose: Main entry point for saving HLOD data to W3D file
- Calls: save_header, save_lod_arrays, save_aggregate_array, save_proxy_array

### HLodSaveClass::save_header
- Purpose: Writes the HLOD header chunk
- Calls: ChunkSaveClass::Begin_Chunk, ChunkSaveClass::Write, ChunkSaveClass::End_Chunk

### HLodSaveClass::save_lod_arrays
- Purpose: Writes all LOD arrays
- Calls: save_sub_object_array

### HLodSaveClass::save_aggregate_array
- Purpose: Saves aggregate objects if any exist
- Calls: save_sub_object_array

### HLodSaveClass::save_proxy_array
- Purpose: Saves proxy objects if any exist
- Calls: save_sub_object_array

### HLodSaveClass::save_sub_object_array
- Purpose: Writes mesh-to-bone connectivity for each sub-object
- Calls: ChunkSaveClass::Begin_Chunk, ChunkSaveClass::Write, ChunkSaveClass::End_Chunk

## Globals
- **header (W3dHLodHeaderStruct)**: Stores HLOD header information
- **lod_array (HLodArrayEntry*)**: Array of LOD entries
- **aggregate_array (HLodArrayEntry)**: Stores aggregate objects
- **proxy_array (HLodArrayEntry)**: Stores proxy objects

## Dependencies
- hlodsave.h, meshcon.h, errclass.h, util.h, w3dappdata.h, wwmath.h, exportlog.h
- ChunkSaveClass, MeshConnectionsClass, INodeListClass, Progress_Meter_Class
- W3D chunk constants and structures
