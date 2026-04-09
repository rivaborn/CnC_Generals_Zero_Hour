# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/buff.cpp

## Purpose
Implements a buffer management class for handling dynamic memory allocation and deallocation.

## Responsibilities
- Manages buffer memory allocation/deallocation
- Provides constructors for different buffer initialization scenarios
- Handles buffer copying and assignment
- Ensures proper cleanup in destructor
- Supports self-allocating buffers

## Key Types
- `Buffer` (Class): Wrapper for buffer memory management
- `BufferPtr` (void*): Pointer to the buffer memory
- `Size` (long): Size of the buffer in bytes
- `IsAllocated` (bool): Flag indicating if buffer was allocated by this object

## Key Functions
### `Buffer::Buffer(void *buffer, long size)`
- Purpose: Constructs a buffer object with external memory
- Calls: `W3DNEWARRAY` (if buffer is NULL and size > 0)

### `Buffer::Buffer(long size)`
- Purpose: Self-allocating constructor that creates buffer memory
- Calls: `W3DNEWARRAY`

### `Buffer::Buffer(Buffer const &buffer)`
- Purpose: Copy constructor that duplicates buffer reference
- Calls: None

### `Buffer &Buffer::operator=(Buffer const &buffer)`
- Purpose: Assignment operator for buffer objects
- Calls: `delete []` (if IsAllocated)

### `Buffer::~Buffer()`
- Purpose: Destructor that cleans up allocated memory
- Calls: `Reset()`

### `void Buffer::Reset()`
- Purpose: Clears buffer object to null state
- Calls: `delete []` (if IsAllocated)

## Globals
None

## Dependencies
- `always.h`
- `buff.h`
- `W3DNEWARRAY` (memory allocation function)
- Standard C++ memory management operators
