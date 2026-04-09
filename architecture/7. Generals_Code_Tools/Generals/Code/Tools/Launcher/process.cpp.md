# Generals/Code/Tools/Launcher/process.cpp

## Purpose
Handles process creation, execution, and monitoring for the game launcher.

## Responsibilities
- Spawn external processes with configurable command lines and working directories
- Wait for process completion and retrieve exit codes
- Parse process launch parameters from configuration files

## Key Types
- Process (Class): encapsulates process state (handles, IDs, command line, args, directory)
- ConfigFile (External): configuration file reader (used in Read_Process_Info)

## Key Functions
### Create_Process
- Purpose: Creates a new process from Process object parameters
- Calls: CreateProcess, DBGMSG, FormatMessage, GetLastError

### Wait_Process
- Purpose: Waits for process termination and retrieves exit code
- Calls: WaitForSingleObject, Sleep, GetExitCodeProcess

### Read_Process_Info
- Purpose: Parses process launch parameters from config file
- Calls: ConfigFile::getString, Wstring methods, DBGMSG

## Globals
- None

## Dependencies
- Windows API: CreateProcess, WaitForSingleObject, GetExitCodeProcess, FormatMessage, GetLastError
- Custom: ConfigFile, Wstring, DBGMSG macro
- Process.h header for Process class definition
