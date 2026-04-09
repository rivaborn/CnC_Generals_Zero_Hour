# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwmemlog.h

## Purpose
Header file defining memory logging utilities for tracking memory allocations by category in the SAGE engine.

## Responsibilities
- Defines memory categories for tracking allocations
- Declares `WWMemoryLogClass` for memory logging management
- Provides `WWMemorySampleClass` for scoped memory category tracking
- Defines `WWMEMLOG` macro for easy memory logging

## Key Types
- `MemLogClass` (Class): Internal memory logging implementation (not defined here)
- `(anonymous enum)` (Enum): Memory allocation categories (e.g., `MEM_GEOMETRY`, `MEM_TEXTURE`)
- `WWMemoryLogClass` (Class): Main memory logging interface
- `WWMemorySampleClass` (Class): RAII wrapper for scoped memory category tracking

## Key Functions
### `WWMemoryLogClass::Enable_Memory_Log`
- Purpose: Enable/disable memory logging
- Calls: None

### `WWMemoryLogClass::Allocate_Memory`
- Purpose: Log memory allocation
- Calls: `Register_Memory_Allocated`

### `WWMemoryLogClass::Release_Memory`
- Purpose: Log memory deallocation
- Calls: `Register_Memory_Released`

### `WWMemoryLogClass::Push_Active_Category`
- Purpose: Push current memory category onto stack
- Calls: None

### `WWMemoryLogClass::Pop_Active_Category`
- Purpose: Pop current memory category from stack
- Calls: None

## Globals
- `WWMemoryLogClass::IsMemoryLogEnabled` (bool): Tracks if memory logging is enabled

## Dependencies
- None (header-only, no external includes)
