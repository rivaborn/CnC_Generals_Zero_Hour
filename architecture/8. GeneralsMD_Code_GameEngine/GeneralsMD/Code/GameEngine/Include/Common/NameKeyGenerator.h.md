# GeneralsMD/Code/GameEngine/Include/Common/NameKeyGenerator.h

## Purpose
Defines a system for converting arbitrary strings into unique integer keys and vice versa.

## Responsibilities
- Manages string-to-key and key-to-string mappings
- Provides global access to the name key generator
- Supports static name key generation
- Handles memory management for bucket entries

## Key Types
- **NameKeyType (Enum)**: Type for name keys (magic cookies)
- **Bucket (Class)**: Stores name-key pairs in a catalog
- **NameKeyGenerator (Class)**: Core class for name-key conversion
- **StaticNameKey (Class)**: Wrapper for static name keys

## Key Functions
### NAMEKEY
- Purpose: Convenience function for string-to-key conversion
- Calls: TheNameKeyGenerator->nameToKey

### KEYNAME
- Purpose: Convenience function for key-to-string conversion
- Calls: TheNameKeyGenerator->keyToName

## Globals
- **TheNameKeyGenerator (NameKeyGenerator*)**: Global instance of the name key generator

## Dependencies
- "Lib/BaseType.h", "Common/SubsystemInterface.h", "Common/GameMemory.h", "Common/AsciiString.h"
- MemoryPoolObject, SubsystemInterface, AsciiString, INI
