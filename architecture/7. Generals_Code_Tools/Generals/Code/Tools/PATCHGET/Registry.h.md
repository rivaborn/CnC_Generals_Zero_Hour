# Generals/Code/Tools/PATCHGET/Registry.h

## Purpose
Provides a simple interface for reading and writing string/unsigned int values to the Windows registry.

## Responsibilities
- Define functions for registry read/write operations
- Support both string and unsigned integer data types
- Provide error handling via boolean return values

## Key Types
None

## Key Functions
### GetStringFromRegistry
- Purpose: Retrieves a string value from the registry
- Calls: Not inferable

### GetUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the registry
- Calls: Not inferable

### SetStringInRegistry
- Purpose: Writes a string value to the registry
- Calls: Not inferable

### SetUnsignedIntInRegistry
- Purpose: Writes an unsigned integer value to the registry
- Calls: Not inferable

## Globals
None

## Dependencies
- `<string>`: for std::string usage
- Windows Registry API (not shown in header)
