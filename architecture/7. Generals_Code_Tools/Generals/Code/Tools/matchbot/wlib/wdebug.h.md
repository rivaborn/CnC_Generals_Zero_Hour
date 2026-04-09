# Generals/Code/Tools/matchbot/wlib/wdebug.h

## Purpose
Provides a debugging framework with message streams for logging debug, info, warning, and error messages.

## Responsibilities
- Manages output streams for different message types (debug, info, warn, error)
- Provides thread-safe message output via semaphore/critical section
- Defines macros for logging messages with file/line info and timestamps
- Supports conditional compilation for debug vs. release builds

## Key Types
- **MsgManager (Class)**: Central manager for debug output streams and configuration
- **OutputDevice (Class)**: Base class for output devices (included from odevice.h)

## Key Functions
### MsgManager::setAllStreams
- Purpose: Sets all message streams to the same output device
- Calls: Not inferable

### MsgManager::ReplaceAllStreams
- Purpose: Replaces all streams with a file output device and optionally copies output
- Calls: Not inferable

### MsgManager::setDebugStream / setInfoStream / setWarnStream / setErrorStream
- Purpose: Sets the output device for the respective message stream
- Calls: Not inferable

### MsgManager::enableDebug / enableInfo / enableWarn / enableError
- Purpose: Enables/disables the respective message stream
- Calls: Not inferable

### MsgManager::debugStream / infoStream / warnStream / errorStream
- Purpose: Returns the output stream for the respective message type
- Calls: Not inferable

## Globals
- **DebugLibSemaphore (Sem4/CritSec)**: Thread synchronization primitive for debug output

## Dependencies
- Key includes: wstypes.h, iostream, strstrea, sem4.h, critsec.h, odevice.h, streamer.h, xtime.h, timezone.h, filed.h
- External symbols: OutputDevice, ostream, Xtime, TimezoneOffset(), OutputDebugString (Windows)
