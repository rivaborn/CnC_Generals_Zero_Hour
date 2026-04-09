# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/agg_def.h

## Purpose
Defines the AggregateDefClass and related structures for managing 3D aggregate objects in the W3D engine.

## Responsibilities
- Defines the AggregateDefClass for describing aggregate objects
- Provides loading/saving functionality for W3D aggregate files
- Manages subobject attachments and texture replacements
- Implements prototype system for aggregate objects
- Handles asset loading and render object creation

## Key Types
- **AggregateDefClass (Class)**: Main class for aggregate object definitions
- **AggregatePrototypeClass (Class)**: Prototype wrapper for aggregate definitions
- **AggregateLoaderClass (Class)**: Loader for aggregate chunks in W3D files
- **_TEXTURE_INFO (Struct)**: Texture replacement information structure
- **ChunkLoadClass (Class)**: Forward declaration for chunk loading
- **ChunkSaveClass (Class)**: Forward declaration for chunk saving
- **IndirectTextureClass (Class)**: Forward declaration for texture handling

## Key Functions
### AggregateDefClass::Load_W3D
- Purpose: Load aggregate data from a W3D chunk
- Calls: Read_Header, Read_Info, Read_Subobject, Read_Class_Info

### AggregateDefClass::Save_W3D
- Purpose: Save aggregate data to a W3D chunk
- Calls: Save_Header, Save_Info, Save_Subobject, Save_Class_Info

### AggregateDefClass::Create
- Purpose: Create a render object from the aggregate definition
- Calls: Create_Render_Object, Attach_Subobjects

### AggregateDefClass::Attach_Subobjects
- Purpose: Attach subobjects to the base model
- Calls: Find_Subobject

### AggregateDefClass::Load_Assets
- Purpose: Load external assets referenced by the aggregate
- Calls: Create_Render_Object

## Globals
- **_AggregateLoader (AggregateLoaderClass)**: Global loader instance for aggregate chunks

## Dependencies
- "proto.h", "rendobj.h", "w3d_file.h", "w3derr.h", "vector.h", "bittype.h"
- DynamicVectorClass, W3dAggregateInfoStruct, W3dAggregateMiscInfo, W3dAggregateSubobjectStruct
- ChunkLoadClass, ChunkSaveClass, IndirectTextureClass (forward declarations)
