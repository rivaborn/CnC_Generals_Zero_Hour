# GeneralsMD/Code/GameEngine/Include/Common/Dict.h

## Purpose
Provides a general-purpose dictionary class for maintaining sorted key-value pairs, supporting various data types.

## Responsibilities
- Manage key-value pairs with NameKeyType keys
- Support multiple data types (bool, int, real, string)
- Maintain sorted order and provide efficient lookup
- Handle reference counting for shared data

## Key Types
- **Dict (Class)**: Main dictionary container class
- **DataType (Enum)**: Defines supported value types (bool, int, real, string)
- **DictPair (Struct)**: Internal structure for storing key-value pairs
- **DictPairData (Struct)**: Reference-counted data container for pairs

## Key Functions
### Dict::setPrep
- Purpose: Prepare a pair for setting a value
- Calls: findPairByKey, ensureUnique

### Dict::findPairByKey
- Purpose: Find a pair by its key using binary search
- Calls: None

### Dict::ensureUnique
- Purpose: Ensure the dictionary has enough capacity for new pairs
- Calls: None

## Globals
- **MAX_LEN (Enum)**: Maximum total length of any Dict in pairs (32767)

## Dependencies
- "Common/Errors.h"
- "Common/NameKeyGenerator.h"
- NameKeyType, AsciiString, UnicodeString types
- Reference counting mechanism for shared data
