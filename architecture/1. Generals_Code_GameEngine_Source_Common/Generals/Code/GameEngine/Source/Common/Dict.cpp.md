# Generals/Code/GameEngine/Source/Common/Dict.cpp

## Purpose
This file implements a general-purpose dictionary class (`Dict`) used for storing key-value pairs with various data types (bool, int, real, ASCII string, Unicode string). It supports operations like adding, retrieving, and removing entries, as well as sorting the dictionary.

## Responsibilities
- Manage dynamic memory allocation for storing dictionary entries.
- Provide methods to add, retrieve, and remove key-value pairs.
- Ensure thread safety through reference counting.
- Support sorting of dictionary entries by keys.

## Key Types
- `DictPair` (struct): Represents a single key-value pair in the dictionary.
  - Purpose: Stores a key, type, and value for each entry.
- `DictPairData` (struct): Manages an array of `DictPair` objects.
  - Purpose: Holds metadata like reference count and allocated/used pair counts.

## Key Functions
### Dict::copyFrom
- Purpose: Copies data from another `DictPair`.
- Calls: `clear`, `asAsciiString`, `asUnicodeString`.

### Dict::clear
- Purpose: Clears the dictionary, releasing all associated memory.
- Calls: `releaseData`.

### Dict::ensureUnique
- Purpose: Ensures that the dictionary has a unique buffer with enough space for new entries.
- Calls: `allocateBytes`, `freeBytes`, `copyFrom`.

### Dict::findPairByKey
- Purpose: Searches for a `DictPair` by key using binary search.
- Calls: None.

### Dict::setBool, setInt, setReal, setAsciiString, setUnicodeString
- Purpose: Sets the value of a key in the dictionary with the specified type and value.
- Calls: `setPrep`, `sortPairs`.

### Dict::remove
- Purpose: Removes a key-value pair from the dictionary.
- Calls: `ensureUnique`, `sortPairs`.

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Dict.h"
  - "Common/GameMemory.h"
- External symbols used but not defined here:
  - `TheDynamicMemoryAllocator`
  - `DEBUG_ASSERTCRASH`
  - `ERROR_OUT_OF_MEMORY`
  - `AsciiString::TheEmptyString`
  - `UnicodeString::TheEmptyString`
