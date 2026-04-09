# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/nstrdup.cpp

## Purpose
Implements a string duplication function using dynamic memory allocation.

## Responsibilities
- Allocates memory for a duplicate string
- Copies the input string into the new memory
- Handles null input gracefully

## Key Types
None

## Key Functions
### nstrdup
- Purpose: Duplicates a string using dynamic memory allocation
- Calls: strlen, strcpy, W3DNEWARRAY

## Globals
None

## Dependencies
- always.h
- string.h
- nstrdup.h
- W3DNEWARRAY (memory allocation macro)
