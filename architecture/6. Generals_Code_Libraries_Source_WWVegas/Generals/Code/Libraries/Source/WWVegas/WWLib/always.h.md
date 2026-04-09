# Generals/Code/Libraries/Source/WWVegas/WWLib/always.h

## Purpose
Provides memory management utilities, operator overloads, and utility macros for the SAGE engine.

## Responsibilities
- Defines custom memory allocation operators for debugging and profiling
- Implements memory pool management for W3D objects
- Provides min/max macros and template functions
- Configures compiler-specific settings and warnings
- Defines utility macros for array size and NULL

## Key Types
- W3DMPO (Class): Base class for memory-pooled objects using W3DMPO_GLUE macro

## Key Functions
### operator new/delete
- Purpose: Custom memory allocation operators for debugging
- Calls: _malloc_dbg/_free_dbg (in debug builds)

### createW3DMemPool
- Purpose: Creates a named memory pool for object allocation
- Calls: Not inferable

### allocateFromW3DMemPool
- Purpose: Allocates memory from a W3D memory pool
- Calls: Not inferable

### freeFromW3DMemPool
- Purpose: Frees memory allocated from a W3D memory pool
- Calls: Not inferable

### min/max (template)
- Purpose: Type-safe min/max functions
- Calls: None

## Globals
- None

## Dependencies
- <assert.h>
- <crtdbg.h> (debug builds)
- <stdlib.h> (debug builds)
- <malloc.h> (debug builds)
- "borlandc.h", "visualc.h", "watcom.h" (compiler-specific)
