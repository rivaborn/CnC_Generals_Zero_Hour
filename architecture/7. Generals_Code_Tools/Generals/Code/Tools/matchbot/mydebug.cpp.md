# Generals/Code/Tools/matchbot/mydebug.cpp

## Purpose
Manages debug output streams and device redirection for the matchbot tool.

## Responsibilities
- Configures and redirects debug output streams
- Manages synchronization via semaphore/critical section
- Handles file device replacement for logging

## Key Types
- `MyMsgManager` (Class): Debug message manager with stream control methods
- `ostream` (Type): Output stream wrapper
- `Streamer` (Type): Streamer interface for output devices
- `OutputDevice` (Type): Abstract output device interface
- `FileD` (Type): File-based output device

## Key Functions
### `setAllStreams`
- Purpose: Sets all debug streams to a specified output device.
- Calls: `MYDEBUGLOCK`, `paranoid_streamer.setOutputDevice`, `delete`, `new`

### `setParanoidStream`
- Purpose: Configures the paranoid debug stream to a specific output device.
- Calls: `MYDEBUGLOCK`, `paranoid_streamer.setOutputDevice`, `delete`, `new`

### `paranoidStream`
- Purpose: Returns the paranoid debug output stream.
- Calls: None

### `ReplaceAllStreams`
- Purpose: Replaces all debug output streams with a new file device.
- Calls: `MYDEBUGLOCK`, `delete`, `rename`, `new`, `paranoid_streamer.setOutputDevice`

## Globals
- `paranoid_ostream` (ostream*): The paranoid debug output stream.
- `paranoid_streamer` (Streamer): Streamer instance for paranoid output.
- `MyDebugLibSemaphore` (Sem4/CritSec): Synchronization primitive for thread safety.

## Dependencies
- `mydebug.h`, `streamer.h`, `odevice.h`
- `ostream`, `Streamer
