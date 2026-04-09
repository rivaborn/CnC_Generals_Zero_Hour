# GeneralsMD/Code/GameEngine/Include/Common/INI.h

## Purpose
Header file defining the INI class and related types for parsing INI configuration files in the game engine.

## Responsibilities
- Declares the INI class for reading and parsing INI files
- Defines parsing functions for various data types
- Provides enums for error codes and parsing options
- Declares helper structures for field parsing

## Key Types
- INI (Class): Main INI file reader class
- INILoadType (Enum): Controls how INI data is loaded
- FieldParse (Struct): Parse table entry for data fields
- MultiIniFieldParse (Class): Handles multiple field parses
- LookupListRec (Struct): Name-value pair for lookup lists

## Key Functions
### parseObjectDefinition
- Purpose: Parses object definition blocks in INI files
- Calls: Not inferable

### parseUnsignedByte
- Purpose: Parses unsigned byte values from INI tokens
- Calls: Not inferable

### getNextToken
- Purpose: Retrieves the next token from the current line
- Calls: Not inferable

### scanInt
- Purpose: Converts token string to integer
- Calls: Not inferable

## Globals
- INI_MAX_CHARS_PER_LINE (Enum): Maximum characters per line (1028)
- INI_READ_BUFFER (Enum): Size of internal read buffer (8192)

## Dependencies
- Common/STLTypedefs.h
- Common/AsciiString.h
- Common/GameCommon.h
- File class
- Xfer class
- ScienceType enum
