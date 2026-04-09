# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/pointerremap.h

## Purpose
Manages pointer remapping during save/load operations to handle memory address changes.

## Responsibilities
- Registers old/new pointer pairs for remapping
- Processes remapping requests for pointers and reference-counted objects
- Maintains tables of pointer pairs and remap requests
- Handles debug information for pointer remapping (in debug builds)

## Key Types
- **RefCountClass (Class)**: Reference-counted object base class
- **PointerRemapClass (Class)**: Main class handling pointer remapping
- **PtrPairStruct (Struct)**: Stores old/new pointer pairs
- **PtrRemapStruct (Struct)**: Stores pointers to remap with optional debug info

## Key Functions
### PointerRemapClass::Register_Pointer
- Purpose: Registers a pair of old and new pointers for remapping
- Calls: None

### PointerRemapClass::Request_Pointer_Remap
- Purpose: Requests remapping of a pointer (with optional debug info)
- Calls: None

### PointerRemapClass::Request_Ref_Counted_Pointer_Remap
- Purpose: Requests remapping of a reference-counted pointer (with optional debug info)
- Calls: None

### PointerRemapClass::Process
- Purpose: Processes all pending remap requests
- Calls: Process_Request_Table

### PointerRemapClass::Process_Request_Table
- Purpose: Processes a table of remap requests
- Calls: None

## Globals
- None

## Dependencies
- Key includes: "always.h", "vector.h"
- External symbols: DynamicVectorClass, RefCountClass
