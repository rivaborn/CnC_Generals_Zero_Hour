# Generals/Code/GameEngine/Source/Common/NameKeyGenerator.cpp

## Purpose
This file implements a name key system to translate between names and unique key IDs, used for efficient lookups in the game engine.

## Responsibilities
- Manages a singleton instance of `NameKeyGenerator`.
- Provides methods to initialize, reset, and free resources.
- Converts strings to unique keys and vice versa using hash tables.
- Handles collisions by chaining buckets within sockets.

## Key Types
- **NameKeyGenerator (Class)**: Manages the name-to-key mapping system.
- **Bucket (Struct)**: Represents a single entry in the hash table.
- **None**: No enums defined in this file.

## Key Functions
### calcHashForString
- Purpose: Calculates a hash value for a given string.
- Calls: None

### NameKeyGenerator::init
- Purpose: Initializes the name key generator system.
- Calls: `freeSockets`

### NameKeyGenerator::reset
- Purpose: Resets the name key generator by freeing all resources and reinitializing.
- Calls: `freeSockets`

### NameKeyGenerator::freeSockets
- Purpose: Frees all allocated buckets in the hash table.
- Calls: `Bucket::deleteInstance`

### NameKeyGenerator::keyToName
- Purpose: Retrieves the name associated with a given key.
- Calls: None

### NameKeyGenerator::nameToKey
- Purpose: Converts a string to a unique key, creating a new entry if necessary.
- Calls: `calcHashForString`, `newInstance`

## Globals
- **TheNameKeyGenerator (NameKeyGenerator*)**: Singleton instance of the name key generator.

## Dependencies
- Key includes:
  - "PreRTS.h"
- External symbols used but not defined here:
  - `DEBUG_ASSERTCRASH`
  - `NAMEKEY_INVALID`
  - `SOCKET_COUNT`
  - `UnsignedInt`
  -
