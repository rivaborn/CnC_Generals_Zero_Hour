# Generals/Code/Tools/CRCDiff/KVPair.h

## Purpose
Defines a key-value pair utility class for parsing and storing string-based configuration data.

## Responsibilities
- Parse key-value pairs from strings or files
- Store data in a map structure
- Retrieve values as strings, integers, or unsigned integers
- Handle delimited input formats

## Key Types
- **KeyValueMap (typedef)**: Alias for `std::map<std::string, std::string>` storing key-value pairs
- **KVPairClass (Class)**: Main class for key-value pair operations

## Key Functions
### KVPairClass()
- Purpose: Default constructor
- Calls: None

### KVPairClass(const std::string& in, const std::string& delim)
- Purpose: Constructor parsing a delimited string into key-value pairs
- Calls: `set()`

### set(const std::string& in, const std::string& delim)
- Purpose: Parses a delimited string into key-value pairs
- Calls: None

### readFromFile(const std::string& in, const std::string& delim)
- Purpose: Reads and parses key-value pairs from a file
- Calls: None

### getStringVal(const std::string& key) const
- Purpose: Retrieves a value as a string
- Calls: None

### getString(const std::string& key, std::string& val) const
- Purpose: Retrieves a value into a string reference
- Calls: None

### getInt(const std::string& key, int& val) const
- Purpose: Retrieves a value as an integer
- Calls: None

### getUnsignedInt(const std::string& key, unsigned int& val) const
- Purpose: Retrieves a value as an unsigned integer
- Calls: None

##
