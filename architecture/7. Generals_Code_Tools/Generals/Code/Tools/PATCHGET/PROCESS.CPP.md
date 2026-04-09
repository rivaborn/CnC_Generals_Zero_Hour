# Generals/Code/Tools/PATCHGET/PROCESS.CPP

## Purpose
This file implements a simple process management utility for launching and monitoring external processes.

## Responsibilities
- Manages process creation, execution, and termination
- Parses process configuration from a config file
- Provides synchronization for process completion
- Handles process exit codes

## Key Types
- Process (Class): wraps process execution state (handles, command, args, directory)
- ConfigFile (External): configuration file parser (used in Read_Process_Info)

## Key Functions
### Process::Process()
- Purpose: Initializes a Process object with default values
- Calls: None

### Create_Process()
- Purpose: Launches an external process using Windows API
- Calls: CreateProcess, ZeroMemory, memset, strcpy, strcat

### Wait_Process()
- Purpose: Blocks until the process completes and retrieves its exit code
- Calls: WaitForSingleObject, GetExitCodeProcess

### Read_Process_Info()
- Purpose: Parses process launch parameters from a config file
- Calls: ConfigFile::getString, Wstring::getToken, Wstring::remove, DBGMSG

## Globals
- None

## Dependencies
- Windows API (CreateProcess, WaitForSingleObject, GetExitCodeProcess)
- Wstring (string handling)
- ConfigFile (configuration parsing)
- DBGMSG (debug output)
