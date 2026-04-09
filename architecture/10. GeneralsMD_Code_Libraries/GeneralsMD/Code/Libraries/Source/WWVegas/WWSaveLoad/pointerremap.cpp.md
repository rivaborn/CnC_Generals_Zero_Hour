# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/pointerremap.cpp

## Purpose
Manages pointer remapping during save/load operations to handle memory address changes.

## Responsibilities
- Registers old/new pointer pairs
- Processes remap requests for regular and ref-counted pointers
- Handles pointer remapping with sorting and binary search
- Provides debug information for failed remaps

## Key Types
- `PointerRemapClass` (Class): Main pointer remapping manager
- `PtrPairStruct` (Struct): Stores old/new pointer pairs
- `PtrRemapStruct` (Struct): Stores pointer remap requests with debug info

## Key Functions
### `Process()`
- Purpose: Processes all pending pointer remap requests
- Calls: `qsort`, `Process_Request_Table`

### `Process_Request_Table()`
- Purpose: Remaps pointers in a request table
- Calls: None directly (uses table access)

### `Register_Pointer()`
- Purpose: Registers an old/new pointer pair for remapping
- Calls: None

### `Request_Pointer_Remap()`
- Purpose: Requests remapping of a regular pointer
- Calls: None

### `Request_Ref_Counted_Pointer_Remap()`
- Purpose: Requests remapping of a ref-counted pointer
- Calls: None

### `ptr_pair_compare_function()`
- Purpose: Comparison function for sorting pointer pairs
- Calls: None

### `ptr_request_compare_function()`
- Purpose: Comparison function for sorting remap requests
- Calls: None

## Globals
- `POINTER_TABLES_GROWTH_STEP` (const int): Growth step size for dynamic tables

## Dependencies
- `pointerremap.h`, `refcount.h`, `wwdebug.h`
- `DynamicVectorClass`, `RefCountClass`, `qsort`, `WWASSERT`, `WWDEBUG_SAY`
