# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/cstraw.h

## Purpose
Defines the `CacheStraw` class, a data transfer regulator in a straw chain that manages buffered data requests.

## Responsibilities
- Regulates data throughput by buffering requests
- Manages a buffer for temporary data storage
- Provides controlled access to buffered data via `Get()`
- Prevents direct copying via private copy constructor/assignment

## Key Types
- **CacheStraw (Class)**: Buffers and regulates data transfer in a straw chain.

## Key Functions
### CacheStraw(Buffer const & buffer)
- Purpose: Constructs a `CacheStraw` with an existing buffer.
- Calls: `BufferPtr(buffer)`, `Index(0)`, `Length(0)`

### CacheStraw(int length=4096)
- Purpose: Constructs a `CacheStraw` with a new buffer of specified size.
- Calls: `BufferPtr(length)`, `Index(0)`, `Length(0)`

### Get(void * source, int slen)
- Purpose: Retrieves data from the buffer into the provided source.
- Calls: Not inferable (implementation in `.cpp` file).

### Is_Valid()
- Purpose: Checks if the underlying buffer is valid.
- Calls: `BufferPtr.Is_Valid()`

### CacheStraw(CacheStraw & rvalue)
- Purpose: Private copy constructor to prevent copying.
- Calls: None

### operator=(CacheStraw const & pipe)
- Purpose: Private assignment operator to prevent copying.
- Calls: None

## Globals
- None

## Dependencies
- `buff.h` (for `Buffer` class)
- `straw.h` (base class `Straw`)
