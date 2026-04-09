# Generals/Code/Tools/Launcher/configfile.cpp

## Purpose
Handles reading and parsing configuration files with key-value pairs.

## Responsibilities
- Parses config files with `#comment` and `key = value` format
- Stores key-value pairs in a dictionary
- Provides retrieval methods for string and integer values
- Handles case insensitivity by converting keys to uppercase

## Key Types
- `ConfigFile` (Class): Main class for config file operations
- `Wstring` (Type): Used for string handling (external)
- `Dictionary` (Type): Hash table for storing key-value pairs (external)

## Key Functions
### `readFile(FILE *in)`
- Purpose: Reads and parses the config file, storing key-value pairs
- Calls: `Eat_Spaces`, `strchr`, `dictionary.add`

### `getString(Wstring &key, Wstring &value)`
- Purpose: Retrieves a config value as a string
- Calls: `dictionary.getValue`

### `getInt(Wstring &key, sint32 &value)`
- Purpose: Retrieves a config value as a 32-bit integer
- Calls: `dictionary.getValue`, `atol`

### `Wstring_Hash(Wstring &string)`
- Purpose: Computes a hash value for a string (static)
- Calls: None

### `Eat_Spaces(char *string)`
- Purpose: Skips leading whitespace in a string (static)
- Calls: `isspace`

## Globals
- None

## Dependencies
- `<stdlib.h>`, `<stdio.h>`, `<ctype.h>`
- `configfile.h` (header)
- `Wstring`, `Dictionary` (external types)
- `bit8`, `sint32`, `sint16`, `uint32` (external types)
