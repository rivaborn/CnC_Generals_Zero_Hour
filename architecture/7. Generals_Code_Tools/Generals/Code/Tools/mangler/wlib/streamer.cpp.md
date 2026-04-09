# Generals/Code/Tools/mangler/wlib/streamer.cpp

## Purpose
Implements a custom stream buffer class for buffered/unbuffered output operations in the mangler tool.

## Responsibilities
- Manages buffered and unbuffered character output
- Handles buffer allocation and flushing
- Integrates with an external `OutputDevice` for actual output
- Provides stream buffer overrides (overflow, underflow, sync)

## Key Types
- **Streamer (class)**: Custom streambuf for output operations.
- **OutputDevice* (member)**: Pointer to the target output device.

## Key Functions
### `Streamer::Streamer()`
- Purpose: Constructor initializes the stream buffer in unbuffered mode.
- Calls: `unbuffered()`

### `Streamer::xsputn(const char* buf, int size)`
- Purpose: Writes a block of characters to the buffer, handling newlines specially.
- Calls: `overflow()`, `sputc()`

### `Streamer::overflow(int c)`
- Purpose: Handles buffer overflow and flushing when needed.
- Calls: `sync()`, `sputc()`

### `Streamer::sync()`
- Purpose: Flushes the buffer to the output device.
- Calls: `Output_Device->print()`

### `Streamer::doallocate()`
- Purpose: Allocates the internal buffer if not already allocated.
- Calls: `setb()`, `setg()`, `setp()`

## Globals
- **STREAMER_BUFSIZ (const)**: Buffer size constant (not defined here).

## Dependencies
- `streamer.h` (header)
- `<windows.h>` (conditional include for Win32)
- `OutputDevice` class (external, used for output)
