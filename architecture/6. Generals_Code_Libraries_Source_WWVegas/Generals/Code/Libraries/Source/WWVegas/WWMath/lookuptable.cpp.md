# Generals/Code/Libraries/Source/WWVegas/WWMath/lookuptable.cpp

## Purpose
Implements lookup table functionality for sampling 1D curves, including serialization and management.

## Responsibilities
- Manages creation and sampling of lookup tables from curves
- Handles loading/saving of lookup tables via chunk I/O
- Provides default table for fallback
- Tracks loaded tables via reference-counted list

## Key Types
- `LookupTableClass` (Class): Stores sampled output values from a curve with input range
- `LookupTableMgrClass` (Class): Manages collection of lookup tables
- `(anonymous enum)` (Enum): Chunk IDs for serialization
- `LOOKUPTABLE_CHUNK_CURVE` (Enum): Curve chunk ID
- `LOOKUPTABLE_CHUNK_EXTENTS` (Enum): Extents chunk ID

## Key Functions
### `LookupTableClass::Init`
- Purpose: Samples a curve and stores output values in the table
- Calls: `curve->Get_Key`, `curve->Evaluate`

### `LookupTableMgrClass::Get_Table`
- Purpose: Retrieves a lookup table by name, loading it if necessary
- Calls: `_TheFileFactory->Get_File`, `Load_Table_Desc`

### `Save_Table_Desc`
- Purpose: Serializes a curve and extents to a chunk stream
- Calls: `csave.Begin_Chunk`, `curve->Get_Factory().Save`

### `Load_Table_Desc`
- Purpose: Deserializes a curve and extents from a chunk stream
- Calls: `SaveLoadSystemClass::Find_Persist_Factory`, `factory->Load`

## Globals
- `LookupTableMgrClass::Tables` (RefMultiListClass<LookupTableClass>): Manages all loaded lookup tables

## Dependencies
- `lookuptable.h`, `curve.h`, `wwfile.h`, `ffactory.h`, `chunkio.h`, `persistfactory.h`, `vector2.h`
- `RefMultiListClass`, `Curve1DClass`, `LinearCurve1DClass`, `ChunkLoadClass`, `ChunkSaveClass`, `PersistFactoryClass`, `SaveLoadSystemClass`
