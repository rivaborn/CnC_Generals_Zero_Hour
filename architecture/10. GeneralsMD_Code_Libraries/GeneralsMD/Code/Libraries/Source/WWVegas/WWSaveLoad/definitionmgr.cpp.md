# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionmgr.cpp

## Purpose
Manages game definitions (e.g., units, buildings) including registration, lookup, and serialization.

## Responsibilities
- Registers/unregisters definitions and maintains sorted array
- Provides lookup methods (by ID, name, or type)
- Handles saving/loading definitions via chunk system
- Generates new unique IDs for definitions
- Supports "twiddling" (randomization) of definitions

## Key Types
- `DefinitionMgrClass` (Class): Singleton manager for game definitions
- `CHUNKID_VARIABLES` (Enum): Chunk ID for variable serialization
- `CHUNKID_OBJECTS` (Enum): Chunk ID for object serialization
- `VARID_NEXTDEFID` (Enum): Variable ID for next definition ID

## Key Functions
### `Find_Definition`
- Purpose: Finds definition by ID using binary search
- Calls: `Get_ID()`, `Twiddle()`

### `Find_Named_Definition`
- Purpose: Finds definition by name via linear search
- Calls: `Get_Name()`, `Twiddle()`

### `Register_Definition`
- Purpose: Adds definition to sorted array with ID validation
- Calls: `Prepare_Definition_Array()`, `Get_ID()`

### `Save_Objects`
- Purpose: Serializes all registered definitions
- Calls: `Is_Save_Enabled()`, `Get_Factory().Save()`

### `Load_Objects`
- Purpose: Deserializes definitions and rebuilds sorted array
- Calls: `SaveLoadSystemClass::Find_Persist_Factory()`, `qsort()`

## Globals
- `_TheDefinitionMgr` (DefinitionMgrClass): Singleton instance
- `DEFINTION_LIST_GROW_SIZE` (int): Growth size for definition array
- `IDRANGE_PER_CLASS` (uint32): ID range per definition class
- `_alloc_time` (float): Allocation timing metric
- `_load_time` (float): Load timing metric
- `_reg_time` (float): Registration timing metric

## Dependencies
- `definition.h`, `definitionfactory.h`, `chunkio.h`
- `wwdebug.h`, `wwmemlog.h`, `twiddler.h`
- `SaveLoadSystemClass`, `PersistFactoryClass`
