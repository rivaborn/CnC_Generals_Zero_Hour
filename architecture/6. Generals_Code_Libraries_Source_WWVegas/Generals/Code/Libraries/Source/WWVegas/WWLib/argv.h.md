# Generals/Code/Libraries/Source/WWVegas/WWLib/argv.h

## Purpose
Command-line argument parsing utility for the game, supporting both direct command-line arguments and loading arguments from a file.

## Responsibilities
- Parse command-line arguments passed to WinMain
- Load and parse argument files (e.g., @file.arg)
- Provide search and iteration functionality for arguments
- Manage argument case sensitivity and exact size matching

## Key Types
- **ArgvClass (Class)**: Main class for argument parsing and management
- **MAX_ARGC (Enum)**: Maximum number of arguments (256)

## Key Functions
### ArgvClass::Init
- Purpose: Initialize the argument parser with command-line and file prefix
- Calls: Not inferable

### ArgvClass::Find
- Purpose: Find an argument in the parsed list
- Calls: Find_Again

### ArgvClass::Find_Value
- Purpose: Get the value associated with an argument
- Calls: Not inferable

### ArgvClass::Update_Value
- Purpose: Update an existing argument's value
- Calls: Not inferable

### ArgvClass::Add_Value
- Purpose: Add a new argument-value pair
- Calls: Not inferable

### ArgvClass::Remove_Value
- Purpose: Remove an argument and its value
- Calls: Not inferable

## Globals
- **Argc (int)**: Static counter for the number of arguments
- **Argv (char*)**: Static array holding argument strings

## Dependencies
- "always.h"
- "osdep.h" (on UNIX)
