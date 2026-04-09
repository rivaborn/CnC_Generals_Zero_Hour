# Generals/Code/Tools/matchbot/wlib/wdebug.cpp

## Purpose
Manages debug message streams and output devices for the matchbot tool.

## Responsibilities
- Configures and replaces debug output streams
- Provides access to debug, info, warn, and error streams
- Handles synchronization for stream operations

## Key Types
- **MsgManager (Class)**: Manages debug message streams and output devices
- **Streamer (Class)**: Not inferable
- **OutputDevice (Class)**: Not inferable
- **FileD (Class)**: Not inferable
- **Sem4/CritSec (Class)**: Synchronization primitives

## Key Functions
### `setAllStreams`
- Purpose: Configures all debug streams to use the same output device
- Calls: `setOutputDevice`, `delete`, `new`

### `ReplaceAllStreams`
- Purpose: Replaces all debug streams with a new output device and renames files
- Calls: `Wait`, `delete`, `rename`, `new`, `Post`

### `setDebugStream`, `setInfoStream`, `setWarnStream`, `setErrorStream`
- Purpose: Configures individual debug streams
- Calls: `setOutputDevice`, `delete`, `new`

### `debugStream`, `infoStream`, `warnStream`, `errorStream`
- Purpose: Returns the corresponding debug stream
- Calls: None

## Globals
- **msg_manager (MsgManager*)**: Global message manager instance
- **debug_enabled (int)**: Flag for debug output
- **debug_ostream (ostream*)**: Debug output stream
- **debug_streamer (Streamer)**: Debug streamer
- **info_enabled (int)**: Flag for info output
- **info_ostream (ostream*)**: Info output stream
- **info_streamer (Streamer)**: Info streamer
- **warn_enabled (int)**: Flag
