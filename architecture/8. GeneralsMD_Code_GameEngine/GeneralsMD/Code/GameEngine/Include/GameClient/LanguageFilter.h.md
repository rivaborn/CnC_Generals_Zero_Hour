# GeneralsMD/Code/GameEngine/Include/GameClient/LanguageFilter.h

## Purpose
Header for the LanguageFilter class, which filters text content (e.g., chat) for inappropriate words.

## Responsibilities
- Define comparison functors for ASCII/Unicode strings
- Declare the LanguageFilter class and its methods
- Provide global access to the language filter instance

## Key Types
- **AsciiStringLessThan (struct)**: Case-insensitive ASCII string comparison
- **UnicodeStringLessThan (struct)**: Case-insensitive Unicode string comparison
- **UnicodeStringsEqual (struct)**: Case-insensitive Unicode string equality check with debug logging
- **LangMap (typedef)**: Map of Unicode strings to booleans for word lists
- **LanguageFilter (class)**: Main filtering subsystem interface

## Key Functions
### createLanguageFilter
- Purpose: Factory function to create a LanguageFilter instance
- Calls: Not inferable

## Globals
- **LANGUAGE_XOR_KEY (const int)**: XOR key for word obfuscation (0x5555)
- **BadWordFileName (const char[])**: Filename for the bad words database ("langdata.dat")
- **TheLanguageFilter (LanguageFilter*)**: Global pointer to the language filter instance

## Dependencies
- Common/STLTypedefs.h
- Common/AsciiString.h
- Common/UnicodeString.h
- File class (forward-declared)
- SubsystemInterface (base class)
- std::map from STL
