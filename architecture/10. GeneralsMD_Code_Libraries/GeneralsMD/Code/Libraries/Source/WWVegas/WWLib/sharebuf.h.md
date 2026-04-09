# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/sharebuf.h

## Purpose
Provides a templated shared buffer class with reference counting for managing arrays of objects shared across different game components.

## Responsibilities
- Manages dynamically allocated arrays with reference counting
- Provides accessor methods for array elements
- Handles memory allocation/deallocation with debug messaging
- Supports copying and clearing of buffer contents

## Key Types
- **ShareBufferClass (Class)**: A reference-counted wrapper for shared arrays of type T

## Key Functions
### ShareBufferClass(int count, const char* msg)
- Purpose: Constructs a new shared buffer with specified count and debug message
- Calls: MSGW3DNEWARRAY

### ShareBufferClass(const ShareBufferClass & that)
- Purpose: Copy constructor that duplicates the source buffer
- Calls: MSGW3DNEWARRAY

### ~ShareBufferClass()
- Purpose: Destructor that cleans up the allocated array
- Calls: delete[]

### Set_Element(int index, const T & thing)
- Purpose: Sets an element at the specified index
- Calls: None

### Get_Element(int index)
- Purpose: Returns a reference to the element at the specified index
- Calls: None

### Clear()
- Purpose: Zeroes out the entire buffer memory
- Calls: memset

## Globals
- None

## Dependencies
- "refcount.h" (RefCountClass)
- MSGW3DNEWARRAY (memory allocation)
- memset (memory clearing)
- assert (debug assertions)
