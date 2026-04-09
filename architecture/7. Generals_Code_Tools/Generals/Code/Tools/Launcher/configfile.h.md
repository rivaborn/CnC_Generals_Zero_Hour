# Generals/Code/Tools/Launcher/configfile.h

## Purpose
Defines the `ConfigFile` class for reading configuration data from files into key-value pairs.

## Responsibilities
- Parses configuration files into a dictionary of key-value pairs.
- Provides methods to retrieve string and integer values by key.
- Supports both `Wstring` and `char*` key types for flexibility.

## Key Types
- **ConfigFile (Class)**: Manages configuration data storage and retrieval.
- **Dictionary<Wstring,Wstring>**: Internal storage for key-value mappings.

## Key Functions
### ConfigFile()
- Purpose: Default constructor.
- Calls: None.

### ~ConfigFile()
- Purpose: Destructor.
- Calls: None.

### readFile(IN FILE *config)
- Purpose: Reads and parses a configuration file.
- Calls: Not inferable (implementation in .cpp).

### getString(IN Wstring &key, OUT Wstring &value)
- Purpose: Retrieves a string value by key.
- Calls: Not inferable.

### getString(IN char *key, OUT Wstring &value)
- Purpose: Retrieves a string value by key (char* variant).
- Calls: Not inferable.

### getInt(IN Wstring &key, OUT sint32 &value)
- Purpose: Retrieves a 32-bit integer value by key.
- Calls: Not inferable.

### getInt(IN char *key, OUT sint32 &value)
- Purpose: Retrieves a 32-bit integer value by key (char* variant).
- Calls: Not inferable.

### getInt(IN Wstring &key, OUT sint16 &value)
- Purpose: Retrieves a 16-bit integer value by key.
- Calls: Not inferable.

### getInt(IN char *key, OUT sint16 &value)
- Purpose: Retrieves
