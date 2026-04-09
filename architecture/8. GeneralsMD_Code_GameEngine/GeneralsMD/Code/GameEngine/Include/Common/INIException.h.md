# GeneralsMD/Code/GameEngine/Include/Common/INIException.h

## Purpose
Defines an exception class for INI file read failures.

## Responsibilities
- Encapsulates error messages for INI parsing failures
- Manages dynamic memory for error strings
- Provides stack-based exception handling

## Key Types
- INIException (Class): Exception class for INI read errors

## Key Functions
### INIException/INIException
- Purpose: Constructor that copies the error message
- Calls: strlen, new, strcpy

### INIException/~INIException
- Purpose: Destructor that cleans up the error message
- Calls: delete[]

## Globals
- None

## Dependencies
- Key includes: Not inferable
- External symbols: strlen, new, strcpy, delete[]
