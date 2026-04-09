# GeneralsMD/Code/GameEngine/Source/Common/NameKeyGenerator.cpp

## Purpose
Implements a name-to-key mapping system for the game engine, allowing string names to be converted to unique integer keys and vice versa.

## Responsibilities
- Manages a hash-based bucket system for storing name-key pairs
- Provides methods to convert between names and keys (case-sensitive and case-insensitive)
- Handles initialization, reset, and cleanup of the key system
- Includes debug checks for hash distribution quality

## Key Types
- **NameKeyGenerator (Class)**: Singleton manager for name-key mappings
- **Bucket (Struct)**: Internal structure holding name-string and key pairs
- **StaticNameKey (Class)**: Wrapper for static name-key associations

## Key Functions
### `calcHashForString`
- Purpose: Computes a hash value for a string
- Calls: None

### `calcHashForLowercaseString`
- Purpose: Computes a case-insensitive hash value for a string
- Calls: `tolower`

### `nameToKey`
- Purpose: Converts a name string to its unique key
- Calls: `calcHashForString`, `newInstance`, `strcmp`

### `nameToLowercaseKey`
- Purpose: Converts a name string to a case-insensitive key
- Calls: `calcHashForLowercaseString`, `newInstance`, `_stricmp`

### `parseStringAsNameKeyType`
- Purpose: Parses an INI value as a name key
- Calls: `TheNameKeyGenerator->nameToKey`

## Globals
- **TheNameKeyGenerator (NameKeyGenerator*)**: Singleton instance of the name key generator

## Dependencies
- `PreRTS.h`, `INI.h`, `AsciiString.h`, `Debug.h`
- Uses `newInstance` and `deleteInstance` for memory management
- Relies on `NAMEKEY_INVALID` constant and `SOCKET_COUNT` macro
