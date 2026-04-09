# GeneralsMD/Code/Libraries/Source/profile/profile_cmd.cpp

## Purpose
Handles command-line interface for profiling functionality in the game engine.

## Responsibilities
- Registers and manages profile result functions
- Executes profiling commands (result, caller, clear, add, view)
- Manages pattern-based inclusion/exclusion lists for profiling
- Provides help documentation for profiling commands

## Key Types
- `ProfileCmdInterface` (Class): Main interface for profile commands
- `Factory` (Struct): Stores function pointer, name, and arguments for result functions
- `ProfileResultInterface` (Pointer): Interface for result output handlers

## Key Functions
### `AddResultFunction`
- Purpose: Registers a new result function with the profiling system
- Calls: `ProfileReAllocMemory`, `strcmp`

### `RunResultFunctions`
- Purpose: Executes all registered result functions at program exit
- Calls: `ProfileResultInterface::WriteResults`, `ProfileResultInterface::Delete`

### `Execute`
- Purpose: Handles command execution for the profile subsystem
- Calls: `Debug::Command`, `ProfileFuncLevelTracer::recordCaller`, `Profile::SimpleMatch`, `ProfileAllocMemory`, `ProfileFreeMemory`

## Globals
- `numResIf` (unsigned): Count of registered result interfaces
- `resIf` (Factory*): Array of registered result interfaces
- `numResFunc` (unsigned): Count of active result functions
- `resFunc` (ProfileResultInterface**): Array of active result functions

## Dependencies
- `_pch.h` (precompiled header)
- `ProfileReAllocMemory`, `ProfileAllocMemory`, `ProfileFreeMemory` (memory functions)
- `Profile::PatternListEntry`, `Profile::SimpleMatch` (pattern matching)
- `ProfileFuncLevelTracer::recordCaller` (caller recording flag)
- `Debug` class (output interface)
