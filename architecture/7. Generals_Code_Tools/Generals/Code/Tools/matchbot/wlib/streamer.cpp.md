# Generals/Code/Tools/matchbot/wlib/streamer.cpp

## Purpose
Implements a custom stream buffer class for buffered/unbuffered output to an external device.

## Responsibilities
- Manages character buffering for output operations
- Handles flushing and synchronization with the output device
- Supports both buffered and unbuffered modes
- Provides stream buffer interface for character output

## Key Types
- **Streamer (class)**: Custom stream buffer for output operations
- **OutputDevice (pointer)**: Interface for external output target

## Key Functions
### Streamer::Streamer()
- Purpose: Constructor initializes stream buffer state
- Calls: unbuffered()

### Streamer::xsputn()
- Purpose: Implements buffered character output
- Calls: sputc(), overflow()

### Streamer::overflow()
- Purpose: Handles buffer overflow and flushing
- Calls: sync(), sputc()

### Streamer::sync()
- Purpose: Flushes buffer contents to output device
- Calls: Output_Device->print()

### Streamer::doallocate()
- Purpose: Allocates buffer memory if needed
- Calls: setb(), setg(), setp()

## Globals
- **Output_Device (OutputDevice*)**: Stores reference to output target

## Dependencies
- `<windows.h>` (Windows-specific)
- `streamer.h` (header with class declaration)
- `OutputDevice` interface (external)
