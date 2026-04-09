# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/FastAllocator.cpp

## Purpose
Implements a fast memory allocator singleton for the game engine.

## Responsibilities
- Manages a global allocator instance
- Initializes allocator pools of varying sizes
- Provides access to the singleton allocator

## Key Types
- None

## Key Functions
### FastAllocatorGeneral::Get_Allocator
- Purpose: Returns the global allocator instance, creating it if necessary
- Calls: `malloc`, placement `new`

### FastAllocatorGeneral::FastAllocatorGeneral
- Purpose: Constructor that initializes allocator pools
- Calls: `Init` on each allocator pool

## Globals
- generalAllocator (FastAllocatorGeneral*): Stores the singleton allocator instance

## Dependencies
- `fastallocator.h`
- `new.h`
- `malloc` from C standard library
