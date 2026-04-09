# Generals/Code/Libraries/Source/WWVegas/WWLib/buff.cpp

## Purpose
Implements a buffer management class for handling dynamic memory allocation and deallocation.

## Responsibilities
- Manages buffer memory allocation/deallocation
- Provides constructors for different buffer initialization scenarios
- Handles buffer copying and assignment
- Ensures proper cleanup in destructor
- Supports self-allocating buffers

## Key Types
- Buffer (Class): wrapper for managing memory buffers with allocation tracking

## Key Functions
### Buffer::Buffer(void * buffer, long size)
- Purpose: Constructs a buffer with external memory
- Calls: W3DNEWARRAY

### Buffer::Buffer(long size)
- Purpose: Self-allocating constructor that creates internal buffer
- Calls: W3DNEWARRAY

### Buffer::Buffer(Buffer const & buffer)
- Purpose: Copy constructor that duplicates buffer reference
- Calls: None

### Buffer & Buffer::operator = (Buffer const & buffer)
- Purpose: Assignment operator for buffer objects
- Calls: delete []

### Buffer::~Buffer(void)
- Purpose: Destructor that cleans up allocated memory
- Calls: Reset()

### void Buffer::Reset(void)
- Purpose: Clears buffer to null state and frees memory if needed
- Calls: delete []

## Globals
None

## Dependencies
- "always.h"
- "buff.h"
- W3DNEWARRAY (memory allocation function)
