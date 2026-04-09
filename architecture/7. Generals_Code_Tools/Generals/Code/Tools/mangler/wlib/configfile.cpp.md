# Generals/Code/Tools/mangler/wlib/configfile.cpp

## Purpose
Handles reading, writing, and managing configuration files with key-value pairs, supporting sections and thread-safe access.

## Responsibilities
- Parse config files into key-value pairs
- Store/retrieve values as strings or integers
- Support section-based organization
- Thread-safe access via critical sections
- Write modified configs back to disk

## Key Types
- **ConfigFile (Class)**: Main class for config file operations
- **Wstring (Type)**: String wrapper used throughout
- **Dictionary_ (Member)**: Hash table storing key-value pairs

## Key Functions
### `readFile(FILE *in)`
- Purpose: Parse a config file into key-value pairs
- Calls: `Eat_Spaces`, `Wstring_Hash`, `Dictionary_::add`

### `getString(IN Wstring &_key, Wstring &value, IN char *section)`
- Purpose: Retrieve a string value by key (case-insensitive)
- Calls: `Dictionary_::getValue`

### `getInt(IN Wstring &_key, sint32 &value, IN char *section)`
- Purpose: Retrieve an integer value by key
- Calls: `Dictionary_::getValue`, `atol`

### `writeFile(FILE *config)`
- Purpose: Write current config state to a file
- Calls: `enumerate`, `fprintf`

### `Wstring_Hash(const Wstring &string)`
- Purpose: Compute hash for string keys
- Calls: None

### `Eat_Spaces(char *string)`
- Purpose: Skip leading whitespace in strings
- Calls: `isspace`

## Globals
- **None**

## Dependencies
- `configfile.h`, `wdebug.h`
- `stdlib.h`, `stdio.h`, `ctype.h`
- `Wstring`, `Dictionary`, `Critsec` (external)
