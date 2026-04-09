# GeneralsMD/Code/GameEngine/Include/Common/Debug.h

## Purpose
Header file defining debug utilities for the game engine, including logging, crashing, and profiling macros.

## Responsibilities
- Defines debug macros and flags for conditional compilation
- Declares debug utility functions (logging, crashing, profiling)
- Provides SimpleProfiler class for performance measurement
- Manages debug output configuration via flags

## Key Types
- AsciiString (Class): Not inferable (forward declared)
- SimpleProfiler (Class): Performance profiling utility
- DEBUG_FLAG_* (Enum): Debug output flags (file, console, timestamp)

## Key Functions
### DebugInit
- Purpose: Initialize debug system with specified flags
- Calls: None

### DebugShutdown
- Purpose: Clean up debug system resources
- Calls: None

### DebugLog
- Purpose: Log debug message with formatting
- Calls: None

### DebugCrash
- Purpose: Trigger a debug crash with formatted message
- Calls: None

### ReleaseCrash
- Purpose: Trigger a crash in release builds
- Calls: None

### ReleaseCrashLocalized
- Purpose: Trigger a localized crash in release builds
- Calls: None

## Globals
- TheCurrentIgnoreCrashPtr (char*): Tracks crash ignore state

## Dependencies
- None (header-only, no external includes)
- Uses AsciiString class (forward declared)
- Relies on C standard library for varargs
