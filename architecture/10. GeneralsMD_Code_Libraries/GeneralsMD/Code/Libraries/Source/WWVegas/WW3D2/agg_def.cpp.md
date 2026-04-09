# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/agg_def.cpp

## Purpose
Implements aggregate definition handling for the W3D rendering system, including loading, saving, and creating hierarchical 3D models.

## Responsibilities
- Manages AggregateDefClass for hierarchical model definitions
- Handles chunk-based loading/saving of aggregate data
- Attaches subobjects to base models
- Provides asset loading and management
- Supports prototype creation for aggregates

## Key Types
- AggregateDefClass (Class): Core class for aggregate definitions
- AggregateLoaderClass (Class): Handles loading aggregates from chunks
- W3dAggregateHeaderStruct (Struct): Header information for aggregates
- W3dAggregateSubobjectStruct (Struct): Subobject attachment data

## Key Functions
### AggregateDefClass::Create
- Purpose: Creates a new aggregate instance from the definition
- Calls: Create_Render_Object, Attach_Subobjects

### AggregateDefClass::Load_W3D
- Purpose: Loads aggregate data from chunk stream
- Calls: Read_Header, Read_Info, Read_Class_Info

### AggregateDefClass::Save_W3D
- Purpose: Saves aggregate data to chunk stream
- Calls: Save_Header, Save_Info, Save_Class_Info

### AggregateDefClass::Attach_Subobjects
- Purpose: Attaches subobjects to base model bones
- Calls: Create_Render_Object

## Globals
- EMPTY_STRING (const char*): Empty string constant
- _AggregateLoader (AggregateLoaderClass): Global aggregate loader instance

## Dependencies
- agg_def.h, htree.h, w3derr.h, chunkio.h, wwdebug.h, assetmgr.h, matinfo.h, texture.h, wwstring.h
- Windows.h for path operations
- WW3DAssetManager for asset loading
- ChunkLoadClass/ChunkSaveClass for serialization
