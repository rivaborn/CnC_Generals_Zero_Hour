# Generals/Code/Tools/Launcher/wdebug.h

## Purpose
Provides a debugging and message logging system for the game, supporting different output streams for debug, info, warning, and error messages.

## Responsibilities
- Manages output streams for different message types
- Provides macros for logging messages with file/line info
- Conditionally compiles debug messages based on DEBUG flag
- Allows enabling/disabling of different message streams

## Key Types
- **MsgManager (Class)**: Central manager for debugging output streams
- **OutputDevice (Class)**: Base class for output devices (external)

## Key Functions
### MsgManager/setAllStreams
- Purpose: Sets all message streams to the same output device
- Calls: None

### MsgManager/setDebugStream
- Purpose: Sets the debug message output stream
- Calls: None

### MsgManager/setInfoStream
- Purpose: Sets the info message output stream
- Calls: None

### MsgManager/setWarnStream
- Purpose: Sets the warning message output stream
- Calls: None

### MsgManager/setErrorStream
- Purpose: Sets the error message output stream
- Calls: None

### MsgManager/enableDebug
- Purpose: Enables/disables debug message output
- Calls: None

### MsgManager/enableInfo
- Purpose: Enables/disables info message output
- Calls: None

### MsgManager/enableWarn
- Purpose: Enables/disables warning message output
- Calls: None

### MsgManager/enableError
- Purpose: Enables/disables error message output
- Calls: None

### MsgManager/debugStream
- Purpose: Returns the debug output stream
- Calls: None

### MsgManager/infoStream
- Purpose: Returns the info output stream
- Calls: None

### MsgManager/warnStream
