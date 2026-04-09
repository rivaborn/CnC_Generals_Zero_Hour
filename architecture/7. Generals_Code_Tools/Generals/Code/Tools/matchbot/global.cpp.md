# Generals/Code/Tools/matchbot/global.cpp

## Purpose
Handles global configuration file reading and string retrieval for the matchbot tool.

## Responsibilities
- Manages a global configuration object
- Reads configuration from files
- Retrieves localized strings with fallback handling

## Key Types
- GlobalClass (Class): Main configuration manager
- config (Not inferable): Internal configuration storage

## Key Functions
### GlobalClass::ReadFile
- Purpose: Reads configuration from a file
- Calls: fopen, config.readFile, fclose

### GlobalClass::GetString
- Purpose: Retrieves a localized string with fallback handling
- Calls: config.getString, Wstring.setFormatted

## Globals
- Global (GlobalClass): Singleton instance of the global configuration manager

## Dependencies
- `<cstdlib>`: For FILE operations
- `"global.h"`: Header for GlobalClass
- `Wstring`: String class used for configuration keys/values
- `config`: External configuration object (not defined here)
