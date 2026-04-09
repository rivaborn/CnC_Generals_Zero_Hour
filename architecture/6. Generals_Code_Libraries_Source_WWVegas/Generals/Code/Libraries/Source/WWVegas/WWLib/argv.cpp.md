# Generals/Code/Libraries/Source/WWVegas/WWLib/argv.cpp

## Purpose
Handles command-line argument parsing and management for the game.

## Responsibilities
- Parses command-line arguments from strings or files
- Supports case-sensitive/exact-size matching
- Manages argument storage and retrieval
- Allows dynamic addition/removal of arguments

## Key Types
- **ArgvClass (Class)**: Main argument parser class
- **MAX_ARGC (const int)**: Maximum argument count limit

## Key Functions
### ArgvClass::Init
- Purpose: Parses command-line arguments from a string
- Calls: Load_File, strdup

### ArgvClass::Find_Again
- Purpose: Searches for arguments with configurable matching
- Calls: strcmp, strncmp, stricmp, strnicmp

### ArgvClass::Load_File
- Purpose: Loads arguments from a configuration file
- Calls: fopen, fgets, strdup

### ArgvClass::Find_Value
- Purpose: Finds argument value by prefix
- Calls: Find, Get_Cur_Value

### ArgvClass::Get_Cur_Value
- Purpose: Extracts value from current argument
- Calls: None

### ArgvClass::Update_Value
- Purpose: Updates or adds argument values
- Calls: Find_Value, free, strdup, memmove

### ArgvClass::Add_Value
- Purpose: Adds new arguments
- Calls: strdup

### ArgvClass::Remove_Value
- Purpose: Removes arguments and their values
- Calls: Find_Value, free, memmove

## Globals
- **Argc (int)**: Current argument count
- **Argv (char*)**: Array of argument strings

## Dependencies
- <assert.h>, <ctype.h>, <stdio.h>, <stdlib.h>, <string.h>
- "ffactory.h", "rawfile.h"
- strdup, strcmp, strncmp, stricmp, strnicmp, fopen, fgets, free, memmove
