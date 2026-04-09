# Generals/Code/Tools/Launcher/streamer.h

## Purpose
Defines a `Streamer` class that provides a `streambuf` interface for outputting text to an `OutputDevice`.

## Responsibilities
- Wraps an `OutputDevice` to provide stream-like output functionality.
- Manages a buffer for efficient character output.
- Implements virtual methods from `streambuf` (`xsputn`, `overflow`, `underflow`, `sync`).
- Allocates and manages its own buffer via `doallocate`.

## Key Types
- **Streamer (Class)**: A `streambuf` subclass that redirects output to an `OutputDevice`.

## Key Functions
### Streamer()
- Purpose: Default constructor.
- Calls: Not inferable.

### ~Streamer()
- Purpose: Destructor.
- Calls: Not inferable.

### setOutputDevice(OutputDevice *output_device)
- Purpose: Sets the target `OutputDevice` for output.
- Calls: Not inferable.

### xsputn(const char* s, int n)
- Purpose: Buffers a block of characters for output.
- Calls: Not inferable.

### overflow(int = EOF)
- Purpose: Flushes the buffer and makes room for more data.
- Calls: Not inferable.

### underflow()
- Purpose: Does nothing (no input support).
- Calls: Not inferable.

### sync()
- Purpose: Flushes the buffer to the `OutputDevice`.
- Calls: Not inferable.

### doallocate()
- Purpose: Allocates the internal buffer.
- Calls: Not inferable.

## Globals
- **STREAMER_BUFSIZ (Macro)**: Defines the buffer size limit (default: 2048).

## Dependencies
- `<stdlib.h>`, `<stdio.h>`, `<stdarg.h>`, `<iostream.h
