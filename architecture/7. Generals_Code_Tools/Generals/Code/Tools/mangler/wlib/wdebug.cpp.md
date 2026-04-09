# Generals/Code/Tools/mangler/wlib/wdebug.cpp

## Purpose
Manages debug message streams and output devices for the toolchain.

## Responsibilities
- Configures debug, info, warning, and error output streams
- Handles stream redirection and device replacement
- Provides thread-safe access to debug streams via semaphore/critical section

## Key Types
- **MsgManager (Class)**: Manages debug message streams and output devices
- **Streamer (Class)**: Underlying stream abstraction (external)
- **OutputDevice (Class)**: Abstract output device (external)
- **FileD (Class)**: File-based output device (external)

## Key Functions
### `setAllStreams`
- Purpose: Configures all debug streams to use the same output device
- Calls: `DEBUGLOCK`, `debug_streamer.setOutputDevice`, `delete`, `new ostream`, `DEBUGUNLOCK`

### `ReplaceAllStreams`
- Purpose: Replaces all output devices and renames log files
- Calls: `DebugLibSemaphore.Wait`, `delete`, `rename`, `new FileD`, `new ostream`, `DebugLibSemaphore.Post`

### `setDebugStream` / `setInfoStream` / `setWarnStream` / `setErrorStream`
- Purpose: Configures individual debug stream output devices
- Calls: `DEBUGLOCK`, `streamer.setOutputDevice`, `delete`, `new ostream`, `DEBUGUNLOCK`

### `debugStream` / `infoStream` / `warnStream` / `errorStream`
- Purpose: Returns the corresponding debug stream
- Calls: None

## Globals
- **msg_manager (MsgManager*)**: Global manager instance
- **debug_enabled/info_enabled/warn_enabled/error_enabled (int)**: Stream enable flags
- **debug_ostream/info_ostream/warn_ostream/error_ostream (ostream*)**: Stream
