# Generals/Code/GameEngine/Source/Common/MiniLog.cpp

## Purpose
This file implements a simple logging system for debugging purposes in the Command & Conquer Generals game engine.

## Responsibilities
- Provides a class `LogClass` to handle log file creation and writing.
- Formats log messages with frame and index information.
- Ensures log entries are written to a specified file.

## Key Types
- LogClass (class): Manages log file operations.

## Key Functions
### LogClass::LogClass(const char *fname)
- Purpose: Initializes the logger by opening a log file.
- Calls: `GetModuleFileName`, `fopen`

### LogClass::~LogClass()
- Purpose: Closes the log file when the logger is destroyed.
- Calls: `fclose`

### LogClass::log(const char *fmt, ...)
- Purpose: Writes formatted messages to the log file with frame and index information.
- Calls: `_vsnprintf`, `fprintf`, `fflush`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/MiniLog.h"
- External symbols used:
  - `GetModuleFileName`
  - `fopen`
  - `fclose`
  - `_vsnprintf`
  - `fprintf`
  - `fflush`
  - `TheGameLogic->getFrame()`
