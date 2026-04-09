# Generals/Code/Tools/WW3D/pluglib/jshell.cpp

## Purpose
Provides utility functions for manipulating bit arrays.

## Responsibilities
- Set individual bits in a bit array
- Retrieve bit values from a bit array
- Find the first set (true) bit in a bit array
- Find the first unset (false) bit in a bit array

## Key Types
None

## Key Functions
### Set_Bit
- Purpose: Sets or clears a specific bit in a bit array
- Calls: None

### Get_Bit
- Purpose: Retrieves the value of a specific bit from a bit array
- Calls: None

### First_True_Bit
- Purpose: Finds the index of the first set bit in a bit array
- Calls: Get_Bit

### First_False_Bit
- Purpose: Finds the index of the first unset bit in a bit array
- Calls: Get_Bit

## Globals
None

## Dependencies
- "always.h" (included header)
- Standard C++ types (void, int, unsigned char)
