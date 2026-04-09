# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionmgr.cpp

## Purpose
Manages game definitions (e.g., units, buildings) including registration, lookup, and serialization.

## Responsibilities
- Registers/unregisters definitions in a sorted array
- Provides lookup methods (by ID, name, or type)
- Handles saving/loading definitions via chunk I/O
- Manages definition IDs and validation

## Key Types
- `DefinitionMgrClass` (Class): Core manager for definitions
- `CHUNKID_VARIABLES`/`CHUNKID_OBJECTS` (Enum): Chunk IDs for serialization
- `VARID_NEXTDEFID` (Enum): Variable ID for next definition ID

## Key Functions
### `Find_Definition`
- Purpose: Finds a definition by ID using binary search
- Calls: `Get_ID()`, `Twiddle()`

### `Register_Definition`
- Purpose: Adds a definition to the sorted array
- Calls: `Prepare_Definition_Array()`, `Get_ID()`

### `Save_Objects`
- Purpose: Serializes all registered definitions
- Calls: `Is_Save_Enabled()`, `Get_Factory().Save()`

### `Load_Objects`
- Purpose: Deserializes definitions and rebuilds the sorted array
- Calls: `SaveLoadSystemClass::Find_Persist_Factory()`, `qsort()`

### `Get_New_ID`
- Purpose: Generates a new unique ID for a given class
- Calls: `Get_ID()`

## Globals
- `_TheDefinitionMgr` (DefinitionMgrClass): Singleton instance
- `DEFINTION_LIST_GROW_SIZE` (int): Growth size for definition array
- `IDRANGE_PER_CLASS` (uint32): ID range per class
- `_alloc_time`/`_load_time`/`_reg_time` (float): Timing metrics

## Dependencies
- `definition.h`, `chunkio.h`, `wwdebug.h`, `wwmemlog.h`
- `HashTemplateClass`, `DynamicVectorClass`, `StringClass`
