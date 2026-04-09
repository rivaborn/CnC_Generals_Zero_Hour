# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/FastAllocator.h

## Purpose
Provides fast memory allocators for the game engine, including stack-based and fixed-size allocators, and STL-compatible allocators.

## Responsibilities
- Implements `StackAllocator` for temporary stack-based memory allocation
- Provides `FastFixedAllocator` for fixed-size memory blocks
- Implements `FastAllocatorGeneral` for variable-sized allocations with bucketing
- Defines `FastSTLAllocator` for STL container optimization
- Tracks memory usage statistics

## Key Types
- **StackAllocator<T, nStackCount, bConstruct> (Class)**: Stack-based allocator for temporary arrays
- **FastFixedAllocator (Class)**: Fixed-size block allocator with chunk management
- **FastAllocatorGeneral (Class)**: General-purpose allocator with size-based bucketing
- **FastSTLAllocator<T> (Class)**: STL-compatible allocator wrapper
- **Link (Struct)**: Internal linked list node for `FastFixedAllocator`
- **Chunk (Struct)**: Memory chunk container for `FastFixedAllocator`

## Key Functions
### StackAllocator::New
- Purpose: Allocates memory from stack or heap based on size
- Calls: Placement `new` for stack allocation, `operator new[]` for heap

### FastFixedAllocator::Alloc
- Purpose: Allocates a fixed-size block from internal pool
- Calls: `grow()` if pool is empty

### FastAllocatorGeneral::Alloc
- Purpose: Allocates memory using size-based bucketing
- Calls: `FastFixedAllocator::Alloc` or `malloc` for large allocations

### FastSTLAllocator::allocate
- Purpose: STL-compatible memory allocation
- Calls: `FastAllocatorGeneral::Alloc`

## Globals
- **FastAllocatorGeneral::Get_Allocator() (Static)**: Returns singleton allocator instance

## Dependencies
- `always.h`, `wwdebug.h`, `mutex.h`
- `<malloc.h>`, `<stddef.h>`, `<string.h>`
- `FastCriticalSectionClass` for thread safety
