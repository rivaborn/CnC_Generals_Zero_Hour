# GeneralsMD/Code/GameEngine/Source/Common/Dict.cpp

## Purpose
Implements a general-purpose dictionary class for storing key-value pairs with various data types.

## Responsibilities
- Manages key-value pairs with types: bool, int, real, ASCII string, Unicode string
- Handles memory allocation and reference counting for dictionary data
- Provides methods for setting, getting, and removing values by key
- Ensures data integrity through validation checks
- Supports copying and merging dictionaries

## Key Types
- **Dict (Class)**: Main dictionary container class
- **DictPair (Struct)**: Represents a single key-value pair
- **DictPairData (Struct)**: Internal data structure for storing pairs
- **DataType (Enum)**: Defines supported data types (DICT_BOOL, DICT_INT, DICT_REAL, DICT_ASCIISTRING, DICT_UNICODESTRING)

## Key Functions
### DictPair::copyFrom
- Purpose: Copies data from another DictPair, handling type conversion
- Calls: clear(), getType(), asAsciiString(), asUnicodeString()

### Dict::findPairByKey
- Purpose: Finds a DictPair by its key using binary search
- Calls: peek(), getName()

### Dict::ensureUnique
- Purpose: Ensures the dictionary has enough capacity and is unique (not shared)
- Calls: releaseData(), TheDynamicMemoryAllocator->allocateBytes(), TheDynamicMemoryAllocator->freeBytes()

### Dict::setPrep
- Purpose: Prepares a DictPair for setting a value, ensuring capacity
- Calls: findPairByKey(), ensureUnique(), setNameAndType(), sortPairs()

### Dict::sortPairs
- Purpose: Sorts dictionary pairs by key using shell sort
- Calls: peek(), getName()

## Globals
- **TheDynamicMemoryAllocator (External)**: Used for memory allocation

## Dependencies
- "Common/Dict.h" (header)
- "Common/GameMemory.h" (for memory allocator)
- AsciiString, UnicodeString (string types)
- DEBUG_ASSERTCRASH, DEBUG_CRASH (debug macros)
