# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwmemlog.h

## Purpose
Header file defining memory logging utilities for tracking memory allocations by category in the SAGE engine.

## Responsibilities
- Defines memory categories for tracking allocations
- Provides interface for memory logging via `WWMemoryLogClass`
- Implements stack-based memory category tracking via `WWMemorySampleClass`
- Defines `WWMEMLOG` macro for scoped memory tracking

## Key Types
- `MemLogClass` (Class): Internal memory log implementation (not shown)
- `(anonymous enum)` (Enum): Memory category identifiers (e.g., `MEM_GEOMETRY`, `MEM_TEXTURE`)
- `WWMemoryLogClass` (Class): Static interface for memory logging and tracking
- `WWMemorySampleClass` (Class): RAII wrapper for scoped memory category tracking

## Key Functions
### `WWMemoryLogClass::Get_Category_Count`
- Purpose: Returns the number of memory categories.
- Calls: None

### `WWMemoryLogClass::Register_Memory_Allocated`
- Purpose: Registers an allocation of a given size.
- Calls: None

### `WWMemoryLogClass::Register_Memory_Released`
- Purpose: Registers a release of memory in a specific category.
- Calls: None

### `WWMemoryLogClass::Allocate_Memory`
- Purpose: Allocates memory and logs it.
- Calls: None

### `WWMemoryLogClass::Release_Memory`
- Purpose: Releases memory and logs it.
- Calls: None

### `WWMemoryLogClass::Push_Active_Category`
- Purpose: Pushes a memory category onto the active stack.
- Calls: None

### `WWMemoryLogClass::Pop_Active_Category`
- Purpose: Pops the active memory category stack.
- Calls:
