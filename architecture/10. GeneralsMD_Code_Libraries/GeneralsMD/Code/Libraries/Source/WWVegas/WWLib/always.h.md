# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/always.h

## Purpose
Provides memory management utilities, operator overloads, and utility macros for the SAGE engine.

## Responsibilities
- Defines custom memory allocation operators (new/delete)
- Implements memory pool management for W3D objects
- Provides min/max macros and template functions
- Includes compiler-specific defines and pragmas
- Defines utility macros (ARRAY_SIZE, size_of)

## Key Types
- W3DMPO (Class): Base class for memory-pooled objects
- min (Template function): Returns the smaller of two values
- max (Template function): Returns the larger of two values

## Key Functions
### operator new/delete
- Purpose: Custom memory allocation operators
- Calls: allocateFromW3DMemPool, freeFromW3DMemPool

### createW3DMemPool
- Purpose: Creates a new memory pool
- Calls: Not inferable

### allocateFromW3DMemPool
- Purpose: Allocates memory from a pool
- Calls: Not inferable

### freeFromW3DMemPool
- Purpose: Frees memory back to a pool
- Calls: Not inferable

## Globals
- None

## Dependencies
- Key includes: `<assert.h>`, `<crtdbg.h>` (debug), `<stdlib.h>`, `<malloc.h>`
- External symbols: `_malloc_dbg`, `_calloc_dbg`, `_realloc_dbg`, `_expand_dbg`, `_free_dbg`, `_msize_dbg` (debug)
