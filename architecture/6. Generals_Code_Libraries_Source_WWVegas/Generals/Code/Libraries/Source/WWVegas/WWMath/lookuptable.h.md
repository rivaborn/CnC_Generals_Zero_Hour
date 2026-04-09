# Generals/Code/Libraries/Source/WWVegas/WWMath/lookuptable.h

## Purpose
Defines lookup table classes for storing and retrieving tabulated function values.

## Responsibilities
- Manages creation and storage of lookup tables
- Provides interpolation methods for table values
- Handles loading/saving of table data
- Tracks active tables via a manager class

## Key Types
- **LookupTableClass (Class)**: Stores tabulated function values with interpolation support
- **LookupTableMgrClass (Class)**: Manages collection of lookup tables
- **Vector2 (Class)**: Forward declaration (external)
- **Curve1DClass (Class)**: Forward declaration (external)
- **ChunkSaveClass (Class)**: Forward declaration (external)
- **ChunkLoadClass (Class)**: Forward declaration (external)

## Key Functions
### LookupTableClass::Get_Value
- Purpose: Interpolates value from table using linear interpolation
- Calls: WWMath::Floor, WWMath::Float_To_Long

### LookupTableClass::Get_Value_Quick
- Purpose: Retrieves nearest table value without interpolation
- Calls: WWMath::Float_To_Long

### LookupTableMgrClass::Get_Table
- Purpose: Retrieves a lookup table by name, optionally loading it
- Calls: None visible

### LookupTableMgrClass::Save_Table_Desc
- Purpose: Saves table description to chunk stream
- Calls: None visible

### LookupTableMgrClass::Load_Table_Desc
- Purpose: Loads table description from chunk stream
- Calls: None visible

## Globals
- **LookupTableMgrClass::Tables (RefMultiListClass<LookupTableClass>)**: Static collection of all active lookup tables

## Dependencies
- "always.h", "simplevec.h", "wwstring.h", "refcount.h",
