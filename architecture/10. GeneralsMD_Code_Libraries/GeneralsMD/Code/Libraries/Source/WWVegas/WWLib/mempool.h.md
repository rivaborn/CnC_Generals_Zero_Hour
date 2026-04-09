# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/mempool.h

## Purpose
Provides object pooling mechanisms for efficient memory management in the game engine.

## Responsibilities
- Implements `ObjectPoolClass` for pre-allocating blocks of objects
- Provides `AutoPoolClass` as a base class for automatic object pooling
- Manages allocation/deallocation with custom `new`/`delete` operators
- Handles thread-safe memory operations via critical sections

## Key Types
- **ObjectPoolClass (Class)**: Manages a pool of objects of type T with block allocation
- **AutoPoolClass (Class)**: Base class that overrides `new`/`delete` to use `ObjectPoolClass`

## Key Functions
### ObjectPoolClass::Allocate_Object
- Purpose: Allocates and constructs an object from the pool
- Calls: `Allocate_Object_Memory`, `new (obj) T`

### ObjectPoolClass::Free_Object
- Purpose: Destroys and returns an object to the pool
- Calls: `obj->T::~T()`, `Free_Object_Memory`

### ObjectPoolClass::Allocate_Object_Memory
- Purpose: Internally allocates raw memory for an object
- Calls: `::operator new`, `FastCriticalSectionClass::LockClass`

### AutoPoolClass::operator new
- Purpose: Overrides global `new` to use the object pool
- Calls: `Allocator.Allocate_Object_Memory()`

### AutoPoolClass::operator delete
- Purpose: Overrides global `delete` to return memory to the pool
- Calls: `Allocator.Free_Object_Memory()`

## Globals
- **DEFINE_AUTO_POOL (Macro)**: Declares the static allocator for `AutoPoolClass`

## Dependencies
- `bittype.h`, `wwdebug.h`, `mutex.h`
- `FastCriticalSectionClass`, `::operator new/delete`
