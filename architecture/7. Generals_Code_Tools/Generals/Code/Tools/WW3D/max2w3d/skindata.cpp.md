# Generals/Code/Tools/WW3D/max2w3d/skindata.cpp

## Purpose
Handles saving and loading skin data for 3D models in MAX file format.

## Responsibilities
- Saves skin data flags, vertex selections, and influence data to MAX files
- Loads skin data from MAX files
- Manages vertex selection sets and influence data structures

## Key Types
- **SkinDataClass (Class)**: Manages skin data serialization
- **InfluenceStruct (Struct)**: Not inferable (used in VertData array)

## Key Functions
### SkinDataClass::Save
- Purpose: Serializes skin data to a MAX file
- Calls: `isave->BeginChunk`, `isave->Write`, `isave->EndChunk`, `VertSel.Save`, `VertData.Addr`

### SkinDataClass::Load
- Purpose: Deserializes skin data from a MAX file
- Calls: `iload->OpenChunk`, `iload->CurChunkID`, `iload->Read`, `iload->CloseChunk`, `VertSel.Load`, `VertSelSets.Load`, `VertData.SetCount`, `VertData.Addr`

## Globals
- **FLAGS_CHUNK (const)**: Chunk ID for flags data
- **VERT_SEL_CHUNK (const)**: Chunk ID for vertex selection data
- **NAMED_SEL_SETS_CHUNK (const)**: Chunk ID for named selection sets
- **INFLUENCE_DATA_CHUNK (const)**: Chunk ID for influence data

## Dependencies
- `skindata.h` (header)
- `ISave`, `ILoad` (MAX file I/O interfaces)
- `BitArrayClass`, `InfluenceStruct` (external types)
