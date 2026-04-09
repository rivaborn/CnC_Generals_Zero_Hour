# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/argv.h

## Purpose
Provides command-line argument parsing functionality, including loading arguments from files.

## Responsibilities
- Parse command-line arguments passed to WinMain
- Load additional arguments from parameter files
- Provide search and iteration capabilities for parsed arguments
- Support case sensitivity and exact size matching options

## Key Types
- **ArgvClass (Class)**: Main class for argument parsing and management
- **MAX_ARGC (Enum)**: Maximum number of arguments (256)
- **(anonymous union)**: Contains flags for case sensitivity and exact size matching
- **(anonymous struct)**: Bitfield for parsing flags

## Key Functions
### ArgvClass::Init
- Purpose: Initialize argument parsing with command line and file prefix
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
- **Argc (int)**: Static counter for number of arguments
- **Argv (char*)**: Static array of argument strings

## Dependencies
- "always.h"
- "osdep.h" (on UNIX)
