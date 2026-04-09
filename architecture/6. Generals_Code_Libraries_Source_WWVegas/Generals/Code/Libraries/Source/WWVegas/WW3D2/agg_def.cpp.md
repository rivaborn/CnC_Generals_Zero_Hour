# Generals/Code/Libraries/Source/WWVegas/WW3D2/agg_def.cpp

## Purpose
Implements aggregate definition loading/saving for the W3D engine, handling hierarchical 3D model composition.

## Responsibilities
- Manages AggregateDefClass for 3D model aggregation
- Handles chunk-based loading/saving of aggregate definitions
- Attaches subobjects to base models
- Manages asset loading through WW3DAssetManager
- Provides prototype creation for aggregates

## Key Types
- AggregateDefClass (Class): Core class for aggregate definitions
- AggregateLoaderClass (Class): Handles aggregate loading
- W3dAggregateHeaderStruct (Struct): Aggregate header data
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

### AggregateLoaderClass::Load_W3D
- Purpose: Factory method for creating aggregate prototypes
- Calls: AggregateDefClass constructor, Load_W3D

## Globals
- EMPTY_STRING (const char*): Empty string constant
- _AggregateLoader (AggregateLoaderClass): Global loader instance

## Dependencies
- agg_def.h, htree.h, w3derr.h, chunkio.h, wwdebug.h, assetmgr.h, matinfo.h, texture.h, wwstring.h
- Windows.h for path operations
- WW3DAssetManager for asset loading
- ChunkLoadClass/ChunkSaveClass for I/O
