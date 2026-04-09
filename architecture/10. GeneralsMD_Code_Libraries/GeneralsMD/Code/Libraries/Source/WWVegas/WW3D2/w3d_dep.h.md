# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3d_dep.h

## Purpose
Header file declaring dependencies for W3D (Westwood 3D) file processing.

## Responsibilities
- Declares `StringList` type alias for dependency tracking
- Declares `Get_W3D_Dependencies` function interface
- Manages include directives and compiler warnings

## Key Types
- StringList (typedef): Alias for `std::list<std::string>` used to store dependency filenames

## Key Functions
### Get_W3D_Dependencies
- Purpose: Retrieves list of dependencies for a given W3D file
- Calls: Not inferable (implementation not shown)

## Globals
- None

## Dependencies
- `<list>` for `std::list`
- `<strstream>` and `<string>` for string handling
- Uses `std::string` and `std::list<std::string>`
