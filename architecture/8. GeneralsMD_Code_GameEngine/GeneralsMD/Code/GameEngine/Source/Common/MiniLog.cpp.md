# GeneralsMD/Code/GameEngine/Source/Common/MiniLog.cpp

## Purpose
Implements a lightweight logging system for debug builds of the game.

## Responsibilities
- Creates log files in the game's executable directory
- Writes formatted log messages with frame/frame-index timestamps
- Manages file handles and cleanup

## Key Types
- LogClass (Class): Debug logging utility

## Key Functions
### LogClass::LogClass
- Purpose: Opens a log file in the game's directory
- Calls: GetModuleFileName, fopen

### LogClass::~LogClass
- Purpose: Closes the log file
- Calls: fclose

### LogClass::log
- Purpose: Writes a formatted message to the log file with frame info
- Calls: TheGameLogic->getFrame, _vsnprintf, fprintf, fflush

## Globals
- None

## Dependencies
- "PreRTS.h", "Common/MiniLog.h"
- GetModuleFileName, fopen, fclose, _vsnprintf, fprintf, fflush
- TheGameLogic (external symbol)
