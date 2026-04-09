# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bfiofile.h

## Purpose
Defines a buffered file I/O class that extends `RawFileClass` for improved read/write performance.

## Responsibilities
- Manages buffered file operations (read/write/seek)
- Handles buffer allocation, caching, and flushing
- Tracks file state (open, cached, modified)
- Provides file metadata access (size, position)

## Key Types
- **BufferIOFileClass (Class)**: Buffered file I/O wrapper.
- **BASECLASS (Class)**: Alias for `RawFileClass` (parent class).
- **(anonymous enum) (Enum)**: Contains `MINIMUM_BUFFER_SIZE` constant.
- **MINIMUM_BUFFER_SIZE (Enum)**: Minimum buffer size (1024 bytes).

## Key Functions
### `Cache`
- Purpose: Activates/deactivates buffering with optional custom buffer.
- Calls: Not inferable.

### `Commit`
- Purpose: Flushes buffered changes to disk.
- Calls: Not inferable.

### `Read`
- Purpose: Reads data from file with buffering.
- Calls: Not inferable.

### `Write`
- Purpose: Writes data to file with buffering.
- Calls: Not inferable.

### `Open` (overloads)
- Purpose: Opens file with specified rights (read/write).
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `rawfile.h` (parent class definition)
- `RawFileClass` (inherited methods)
