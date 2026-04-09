# Generals/Code/Libraries/Source/WWVegas/WWLib/mempool.h

## Purpose
Provides object pooling mechanisms for efficient memory management in the game engine.

## Responsibilities
- Implements `ObjectPoolClass` for managing blocks of objects.
- Provides `AutoPoolClass` for automatic pooling via operator overloading.
- Handles allocation and deallocation of objects in bulk.
- Tracks free and total object counts for memory management.

## Key Types
- **ObjectPoolClass (Class)**: Manages a pool of objects of type T, allocating/deallocating in blocks.
- **AutoPoolClass (Class)**: Base class that overrides `new`/`delete` to use an internal `ObjectPoolClass`.

## Key Functions
### ObjectPoolClass::Allocate_Object
- Purpose: Allocates and constructs an object from the pool.
- Calls: `Allocate_Object_Memory`, `new (obj) T`

### ObjectPoolClass::Free_Object
- Purpose: Destroys and frees an object back to the pool.
- Calls: `obj->T::~T()`, `Free_Object_Memory`

### ObjectPoolClass::Allocate_Object_Memory
- Purpose: Internally allocates raw memory for an object or a new block.
- Calls: `::operator new`

### ObjectPoolClass::Free_Object_Memory
- Purpose: Returns object memory to the free list.
- Calls: None.

### AutoPoolClass::operator new
- Purpose: Overrides `new` to allocate from the pool.
- Calls: `Allocator.Allocate_Object_Memory()`

### AutoPoolClass::operator delete
- Purpose: Overrides `delete` to free memory back to the pool.
- Calls: `Allocator.Free_Object_Memory()`

## Globals
- **DEFINE_AUTO_POOL (Macro)**: Declares the static allocator for `AutoPoolClass`.

## Dependencies
- `bittype.h`, `wwdebug.h`, `<stdlib.h>`, `<stddef.h>`
- `::operator new`, `::operator delete` (global allocators).
