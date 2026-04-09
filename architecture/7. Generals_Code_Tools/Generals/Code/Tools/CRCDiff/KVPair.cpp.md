# Generals/Code/Tools/CRCDiff/KVPair.cpp

## Purpose
Implements a key-value pair parser class for configuration/data files.

## Responsibilities
- Parses string data into key-value pairs
- Reads key-value pairs from files
- Provides accessors for string/int/unsigned int values
- Handles string trimming and delimiter processing

## Key Types
- `KVPairClass` (Class): Main key-value pair container
- `KeyValueMap` (Type): Map of string keys to string values

## Key Functions
### `intToString`
- Purpose: Converts an integer to its string representation
- Calls: None

### `trim`
- Purpose: Removes leading/trailing characters from a string
- Calls: None

### `parseIntoKVPairs`
- Purpose: Parses a string into key-value pairs using delimiters
- Calls: `trim`

### `KVPairClass::set`
- Purpose: Parses input string into key-value pairs
- Calls: `parseIntoKVPairs`

### `KVPairClass::readFromFile`
- Purpose: Reads and parses a file into key-value pairs
- Calls: `set`, `fopen`, `fseek`, `ftell`, `fread`, `fclose`

### `KVPairClass::getStringVal`
- Purpose: Retrieves a string value by key
- Calls: None

### `KVPairClass::getInt`
- Purpose: Retrieves an integer value by key
- Calls: `getStringVal`, `atoi`

### `KVPairClass::getUnsignedInt`
- Purpose: Retrieves an unsigned integer value by key
- Calls: `getStringVal`, `atoi`

## Globals
- None

## Dependencies
- `misc.h`, `KVP
