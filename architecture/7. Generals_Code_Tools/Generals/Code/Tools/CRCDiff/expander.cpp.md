# Generals/Code/Tools/CRCDiff/expander.cpp

## Purpose
Handles template expansion for key/value pairs in strings using marker delimiters.

## Responsibilities
- Parses input strings for marked keys
- Replaces keys with corresponding values
- Supports nested expansions
- Optionally strips unknown keys

## Key Types
- **Expander (Class)**: Manages template expansion logic
- **ExpansionMap (Type)**: Maps keys to replacement strings

## Key Functions
### `addExpansion`
- Purpose: Adds a key/value pair to the expansion map
- Calls: None

### `expand`
- Purpose: Processes input string, replacing marked keys with values
- Calls: `find`, `substr`, recursive `expand`

## Globals
- None

## Dependencies
- `<string>` (std::string)
- "debug.h" (DEBUG_LOG)
- "expander.h" (Expander class definition)
