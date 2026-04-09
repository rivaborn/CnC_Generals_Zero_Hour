# Generals/Code/Tools/matchbot/wlib/configfile.cpp

## Purpose
Handles reading, writing, and managing configuration files with key-value pairs, supporting sections and comments.

## Responsibilities
- Parse config files into key-value pairs
- Store and retrieve values by key (case-insensitive)
- Support section-based organization
- Write modified configs back to disk
- Thread-safe access via critical sections

## Key Types
- **ConfigFile (Class)**: Main class for config file operations
- **Wstring (Type)**: String wrapper used throughout
- **Dictionary_ (Member)**: Hash table storing key-value pairs

## Key Functions
### `readFile(FILE *in)`
- Purpose: Parse a config file into key-value pairs
- Calls: `Eat_Spaces`, `Wstring_Hash`, `Dictionary_::add`

### `getString(IN Wstring &_key, Wstring &value, IN char *section)`
- Purpose: Retrieve a string value by key (optionally scoped to section)
- Calls: `Dictionary_::getValue`

### `setString(IN Wstring &_key, IN Wstring &value, IN char *section)`
- Purpose: Set/update a string value in the config
- Calls: `Dictionary_::remove`, `Dictionary_::add`

### `writeFile(FILE *config)`
- Purpose: Write current config state to a file
- Calls: `enumerate`, `fprintf`

### `Wstring_Hash(const Wstring &string)`
- Purpose: Compute hash for string keys
- Calls: None

### `Eat_Spaces(char *string)`
- Purpose: Skip leading whitespace in strings
- Calls: None

## Globals
- **None**

## Dependencies
- `configfile.h` (header)
- `wdebug.h` (for logging)
- `stdlib.h`, `stdio.h`, `ctype.h` (standard C libs)
- `Dictionary_` (hash table implementation)
- `Critsec_` (critical section for threading)
