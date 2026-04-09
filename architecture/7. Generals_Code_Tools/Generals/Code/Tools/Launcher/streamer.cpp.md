# Generals/Code/Tools/Launcher/streamer.cpp

## Purpose
Implements a custom stream buffer class for buffered/unbuffered output to an external device.

## Responsibilities
- Manages character buffering for output operations
- Handles flushing and synchronization with the output device
- Supports both buffered and unbuffered modes
- Allocates and deallocates internal buffers

## Key Types
- **Streamer (class)**: Custom streambuf derivative for output streaming
- **OutputDevice (pointer)**: Abstract output target interface

## Key Functions
### `Streamer::Streamer()`
- Purpose: Constructor initializes stream buffer state
- Calls: `unbuffered()`

### `Streamer::xsputn(const char* buf, int size)`
- Purpose: Writes a block of characters to the buffer
- Calls: `overflow()`, `sputc()`

### `Streamer::overflow(int c)`
- Purpose: Handles buffer overflow and character output
- Calls: `sync()`, `sputc()`

### `Streamer::sync()`
- Purpose: Flushes buffer contents to the output device
- Calls: `Output_Device->print()`

### `Streamer::doallocate()`
- Purpose: Allocates internal buffer if not already present
- Calls: `setb()`, `setg()`, `setp()`

## Globals
- **Output_Device (OutputDevice*)**: Pointer to the target output device

## Dependencies
- `<windows.h>` (Windows-specific)
- `streamer.h` (header with class declaration)
- `OutputDevice` interface (external)
