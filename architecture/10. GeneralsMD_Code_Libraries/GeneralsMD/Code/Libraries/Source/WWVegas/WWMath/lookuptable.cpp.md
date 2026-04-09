# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/lookuptable.cpp

## Purpose
Implements lookup table functionality for 1D curves, including management, serialization, and evaluation.

## Responsibilities
- Manages creation and storage of lookup tables from curves
- Handles loading/saving of lookup tables via chunk I/O
- Provides default table for fallback
- Evaluates sampled curve values

## Key Types
- LookupTableClass (Class): wraps a sampled 1D curve for fast evaluation
- LookupTableMgrClass (Class): manages collection of lookup tables
- (anonymous enum) (Enum): defines chunk IDs for serialization
- LOOKUPTABLE_CHUNK_CURVE (Enum): curve chunk ID
- LOOKUPTABLE_CHUNK_EXTENTS (Enum): extents chunk ID

## Key Functions
### LookupTableClass::Init
- Purpose: Initializes table by sampling a curve
- Calls: Curve1DClass::Get_Key, Curve1DClass::Evaluate

### LookupTableMgrClass::Get_Table
- Purpose: Retrieves or loads a lookup table by name
- Calls: _TheFileFactory->Get_File, ChunkLoadClass methods, Load_Table_Desc

### Save_Table_Desc
- Purpose: Serializes curve and extents to chunk stream
- Calls: ChunkSaveClass methods, PersistFactoryClass::Save

### Load_Table_Desc
- Purpose: Deserializes curve and extents from chunk stream
- Calls: ChunkLoadClass methods, SaveLoadSystemClass::Find_Persist_Factory

## Globals
- LookupTableMgrClass::Tables (RefMultiListClass<LookupTableClass>): manages all lookup tables

## Dependencies
- lookuptable.h, curve.h, wwfile.h, ffactory.h, chunkio.h, persistfactory.h, vector2.h
- RefMultiListClass, Curve1DClass, LinearCurve1DClass, FileClass, ChunkLoadClass, ChunkSaveClass, PersistFactoryClass, SaveLoadSystemClass
