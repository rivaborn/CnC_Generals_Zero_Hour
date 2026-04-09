# Generals/Code/Tools/Launcher/wdebug.cpp

## Purpose
Manages debug message streams for different log levels (debug, info, warn, error) in the game launcher.

## Responsibilities
- Maintains separate output streams for different log levels
- Allows dynamic reassignment of output devices for each stream
- Provides access to the configured streams via MsgManager methods

## Key Types
- MsgManager (Class): Manages debug message streams and their output devices
- Streamer (Class): Handles stream output to an OutputDevice (external)
- ostream (Class): Standard output stream wrapper (external)

## Key Functions
### MsgManager::setAllStreams
- Purpose: Configures all message streams to use the same output device
- Calls: setOutputDevice, delete, new

### MsgManager::setDebugStream
- Purpose: Configures the debug stream's output device
- Calls: setOutputDevice, delete, new

### MsgManager::setInfoStream
- Purpose: Configures the info stream's output device
- Calls: setOutputDevice, delete, new

### MsgManager::setWarnStream
- Purpose: Configures the warning stream's output device
- Calls: setOutputDevice, delete, new

### MsgManager::setErrorStream
- Purpose: Configures the error stream's output device
- Calls: setOutputDevice, delete, new

### MsgManager::debugStream
- Purpose: Returns the debug output stream
- Calls: None

### MsgManager::infoStream
- Purpose: Returns the info output stream
- Calls: None

### MsgManager::warnStream
- Purpose: Returns the warning output stream
- Calls: None

### MsgManager::errorStream
- Purpose: Returns the error output stream
- Calls: None

## Globals
- msg_manager (MsgManager*): Global instance
