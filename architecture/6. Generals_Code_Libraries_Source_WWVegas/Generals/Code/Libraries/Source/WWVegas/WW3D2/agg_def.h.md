# Generals/Code/Libraries/Source/WWVegas/WW3D2/agg_def.h

## Purpose
Defines the AggregateDefClass and related classes for handling 3D aggregate objects in the W3D engine.

## Responsibilities
- Defines the AggregateDefClass for describing aggregate objects (hierarchy models with subobjects).
- Provides loading/saving functionality for W3D aggregate files.
- Manages subobject attachment and asset loading for aggregates.
- Declares AggregatePrototypeClass for prototype management.
- Declares AggregateLoaderClass for W3D chunk loading.

## Key Types
- **AggregateDefClass (Class)**: Core class for aggregate object definitions.
- **AggregatePrototypeClass (Class)**: Prototype wrapper for AggregateDefClass.
- **AggregateLoaderClass (Class)**: W3D chunk loader for aggregates.
- **_TEXTURE_INFO (Struct)**: Texture replacement information structure.
- **ChunkLoadClass (Class)**: Forward declaration for chunk loading.
- **ChunkSaveClass (Class)**: Forward declaration for chunk saving.
- **IndirectTextureClass (Class)**: Forward declaration for texture handling.

## Key Functions
### AggregateDefClass::Load_W3D
- Purpose: Load aggregate data from a W3D chunk.
- Calls: Read_Header, Read_Info, Read_Subobject, Read_Class_Info

### AggregateDefClass::Save_W3D
- Purpose: Save aggregate data to a W3D chunk.
- Calls: Save_Header, Save_Info, Save_Subobject, Save_Class_Info

### AggregateDefClass::Create
- Purpose: Create a RenderObjClass instance from the aggregate definition.
- Calls: Create_Render_Object, Attach_Subobjects

### AggregateDefClass::Attach_Subobjects
- Purpose: Attach subobjects to the base model.
- Calls: Find_Subobject

### AggregateLoaderClass::Load_W3D
- Purpose: Load aggregate prototype from W3D chunk.
- Calls: AggregateDefClass constructor

## Globals
- **_AggregateLoader (AggregateLoaderClass)**: Global instance for aggregate loading.

## Dependencies
- Key includes: "proto.h", "rendobj.h", "w3d_file.h", "w3derr.h", "vector.h", "bittype.h"
- External symbols: W3DNEW, DynamicVectorClass, W3dAggregateSubobjectStruct, W3dAggregateInfoStruct, W3dAggregateMiscInfo, W3dTextureReplacerStruct
