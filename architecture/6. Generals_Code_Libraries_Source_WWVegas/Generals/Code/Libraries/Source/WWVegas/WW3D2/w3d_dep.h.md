# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3d_dep.h

## Purpose
Header file declaring dependencies for W3D (Westwood 3D) file processing.

## Responsibilities
- Declares a string list type for dependency tracking
- Provides a function to retrieve W3D file dependencies
- Manages include directives and compiler warnings

## Key Types
- StringList (typedef): Alias for std::list<std::string> used to store dependency filenames

## Key Functions
### Get_W3D_Dependencies
- Purpose: Retrieves a list of files depended upon by a W3D file
- Calls: None visible in header

## Globals
- None

## Dependencies
- <list> (STL)
- <strstream> (STL)
- <string> (STL)
