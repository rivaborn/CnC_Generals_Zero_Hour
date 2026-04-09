# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/argv.cpp

## Purpose
Handles command-line argument parsing and manipulation for the game engine.

## Responsibilities
- Parses command-line arguments from strings or files
- Supports case-sensitive/exact-size matching
- Manages argument storage and retrieval
- Provides utilities for adding/removing/updating arguments

## Key Types
- **ArgvClass (Class)**: Main argument parser class
- **MAX_ARGC (const int)**: Maximum argument count (256)

## Key Functions
### ArgvClass::Init
- Purpose: Parses command-line arguments from a string
- Calls: Load_File, strdup

### ArgvClass::Find_Again
- Purpose: Searches for an argument with configurable matching
- Calls: strcmp, strncmp, stricmp, strnicmp

### ArgvClass::Load_File
- Purpose: Loads arguments from a file
- Calls: fopen, fgets, strdup

### ArgvClass::Find_Value
- Purpose: Finds value associated with an argument prefix
- Calls: Find, Get_Cur_Value

### ArgvClass::Get_Cur_Value
- Purpose: Extracts value from current argument
- Calls: strlen, isgraph

### ArgvClass::Update_Value
- Purpose: Updates or adds an argument value
- Calls: Find_Value, free, strdup, memmove, Add_Value

### ArgvClass::Add_Value
- Purpose: Adds new argument and optional value
- Calls: strdup

### ArgvClass::Remove_Value
- Purpose: Removes argument and its value
- Calls: Find_Value, free, memmove

## Globals
- **Argc (int)**: Current argument count
- **Argv (char*)**: Array of argument strings

## Dependencies
- <assert.h>, <ctype.h>, <stdio.h>, <stdlib.h>, <string.h>
- "ffactory.h", "rawfile.h"
- strdup, strcmp, strncmp, stricmp, strnicmp, fopen, fgets, free, memmove
