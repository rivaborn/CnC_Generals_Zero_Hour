# Generals/Code/GameEngine/Source/GameClient/GameText.cpp

## Purpose
Manages game text resources, including localization strings and speech files, providing lookup functionality for UI and game logic.

## Responsibilities
- Loads and parses text files (both plain text and CSF format)
- Provides string lookup by label
- Handles missing string tracking
- Supports map-specific text overrides
- Manages language-specific text resources

## Key Types
- **StringInfo (struct)**: Stores label, text, and speech file associations
- **StringLookUp (struct)**: Lookup table entry for binary search
- **CSFHeader (struct)**: Header structure for CSF (Compiled String File) format
- **NoString (struct)**: Tracks missing strings
- **GameTextManager (class)**: Main text management class implementing GameTextInterface

## Key Functions
### GameTextManager::init
- Purpose: Initializes the text system and loads appropriate string files
- Calls: getStringCount, getCSFInfo, parseStringFile, parseCSF

### GameTextManager::fetch
- Purpose: Retrieves Unicode string by label
- Calls: bsearch, compareLUT

### GameTextManager::parseStringFile
- Purpose: Parses plain text string files
- Calls: readLine, removeLeadingAndTrailing, readToEndOfQuote, translateCopy

### GameTextManager::parseCSF
- Purpose: Parses compiled string files
- Calls: readChar, readLine

### compareLUT
- Purpose: Comparison function for binary search of string lookup table
- Calls: None

## Globals
- **TheGameText (GameTextInterface*)**: Global text interface instance
- **g_strFile (const Char*)**: Path to string file
- **g_csfFile (const Char*)**: Path to CSF file
- **g_useStringFile (Bool)**: Debug flag for string file usage

## Dependencies
- GameClient/GameText.h
- Common/Language.h
- Common/Registry.h
- Common/Debug.h
- Common/UnicodeString.h
- Common/AsciiString.h
- Common/GlobalData.h
- Common/File.h
- Common/FileSystem.h
- Common/LanguageFilter.h (for map strings)
