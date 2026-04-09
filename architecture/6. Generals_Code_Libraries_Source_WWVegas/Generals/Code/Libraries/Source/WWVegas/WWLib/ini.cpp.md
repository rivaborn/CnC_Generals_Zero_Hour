# Generals/Code/Libraries/Source/WWVegas/WWLib/ini.cpp

## Purpose
Handles INI file parsing, storage, and retrieval for the game engine.

## Responsibilities
- Load/save INI data from/to files or streams
- Store/retrieve various data types (strings, integers, floats, points, rectangles, etc.)
- Manage INI sections and entries with indexing
- Handle encoded data blocks and public keys

## Key Types
- INIClass: Main INI file handler
- INISection: Represents a section in INI file
- INIEntry: Represents an entry in a section
- TPoint2D/TPoint3D: Point data structures

## Key Functions
### Load
- Purpose: Load INI data from a file or stream
- Calls: Read_Line, Strip_Comments, CRC

### Get_String
- Purpose: Retrieve a string value from specified section/entry
- Calls: Find_Section, Find_Entry

### Put_String
- Purpose: Store a string value in specified section/entry
- Calls: Find_Section, Add_Entry

### Get_Point
- Purpose: Retrieve point data (2D/3D) from INI
- Calls: Get_String

### Put_Point
- Purpose: Store point data (2D/3D) in INI
- Calls: Put_String

### Get_PKey
- Purpose: Retrieve public key from INI
- Calls: Get_UUBlock

### Put_PKey
- Purpose: Store public key in INI
- Calls: Put_UUBlock

## Globals
- None

## Dependencies
- Key includes: ini.h, straw.h, wwfile.h, pk.h, trect.h, wwstring.h
- External symbols: W3DNEW, OutputDebugString, assert, sprintf, strchr, strlen, strtrim, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, strtod, strcasecmp, strncasecmp, strncmp, strncpy, strstr, strtol, strtoul, str
