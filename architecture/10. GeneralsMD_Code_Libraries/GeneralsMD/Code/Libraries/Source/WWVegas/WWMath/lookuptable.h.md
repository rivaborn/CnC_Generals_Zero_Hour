# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/lookuptable.h

## Purpose
Defines lookup table classes for storing and retrieving tabulated function values.

## Responsibilities
- Manages lookup tables for function interpolation
- Provides table creation, retrieval, and cleanup
- Supports serialization of table data
- Handles table lifecycle via reference counting

## Key Types
- **LookupTableClass (Class)**: Stores tabulated function values with interpolation support
- **LookupTableMgrClass (Class)**: Manages collection of lookup tables
- **Vector2 (Class)**: Forward declaration (external)
- **Curve1DClass (Class)**: Forward declaration (external)
- **ChunkSaveClass (Class)**: Forward declaration (external)
- **ChunkLoadClass (Class)**: Forward declaration (external)

## Key Functions
### LookupTableClass::Get_Value
- Purpose: Interpolates value from lookup table with bounds checking
- Calls: WWMath::Floor, WWMath::Float_To_Long

### LookupTableClass::Get_Value_Quick
- Purpose: Performs fast lookup without interpolation
- Calls: WWMath::Float_To_Long

### LookupTableMgrClass::Get_Table
- Purpose: Retrieves lookup table by name, optionally loading from file
- Calls: Not inferable

### LookupTableMgrClass::Save_Table_Desc
- Purpose: Serializes curve and bounds data to chunk stream
- Calls: Not inferable

### LookupTableMgrClass::Load_Table_Desc
- Purpose: Deserializes curve and bounds data from chunk stream
- Calls: Not inferable

## Globals
- **Tables (RefMultiListClass<LookupTableClass>)**: Static collection of all loaded lookup tables

## Dependencies
- "always.h", "simplevec.h", "wwstring.h", "ref
