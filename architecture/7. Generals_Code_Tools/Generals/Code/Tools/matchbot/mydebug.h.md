# Generals/Code/Tools/matchbot/mydebug.h

## Purpose
Header file defining a debug message manager class and related macros for logging and output streams.

## Responsibilities
- Declares `MyMsgManager` class for managing debug output streams
- Defines macros for paranoid-level debugging messages (`PARANOIDMSG`, `PARANOIDSTREAM`)
- Provides thread-synchronization mechanisms for debug output
- Declares global synchronization primitive (`MyDebugLibSemaphore`)

## Key Types
- **MyMsgManager (Class)**: Manages debug output streams and paranoid logging
- **OutputDevice (Class)**: Base class for output devices (external)
- **FileD (Class)**: File output device (external)

## Key Functions
### MyMsgManager::setAllStreams
- Purpose: Sets all debug streams to the specified output device
- Calls: None visible

### MyMsgManager::setParanoidStream
- Purpose: Sets the paranoid stream to the specified output device
- Calls: None visible

### MyMsgManager::ReplaceAllStreams
- Purpose: Replaces all streams with a file output device and copies output
- Calls: None visible

### MyMsgManager::enableParanoid
- Purpose: Enables or disables paranoid-level logging
- Calls: None visible

### MyMsgManager::paranoidStream
- Purpose: Returns the current paranoid stream
- Calls: None visible

## Globals
- **MyDebugLibSemaphore (Sem4/CritSec)**: Thread synchronization primitive for debug output

## Dependencies
- `wstypes.h`, `iostream.h`/`iostream`, `strstrea.h`, `sem4.h`, `critsec.h`, `odevice.h`, `streamer.h`, `xtime.h`, `timezone.h`, `filed.h`
- `OutputDevice`, `
