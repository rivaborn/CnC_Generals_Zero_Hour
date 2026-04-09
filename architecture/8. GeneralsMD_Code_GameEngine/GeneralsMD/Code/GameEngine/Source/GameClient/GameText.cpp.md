# GeneralsMD/Code/GameEngine/Source/GameClient/GameText.cpp

## Purpose
Manages game text resources, including localization strings and speech files.

## Responsibilities
- Loads and parses text files (CSF and string formats)
- Provides string lookup by label
- Handles missing strings and localization
- Supports map-specific text overrides

## Key Types
- **StringInfo (struct)**: Stores label, text, and speech for a string entry
- **StringLookUp (struct)**: Lookup table entry mapping label to StringInfo
- **CSFHeader (struct)**: Header structure for CSF (Compiled String File) format
- **NoString (struct)**: Linked list node for tracking missing strings
- **GameTextManager (class)**: Main text management class implementing GameTextInterface

## Key Functions
### GameTextManager::init
- Purpose: Initializes the text system by loading string files
- Calls: getStringCount, getCSFInfo, parseStringFile, parseCSF, qsort

### GameTextManager::fetch
- Purpose: Retrieves a Unicode string by its label
- Calls: bsearch, compareLUT

### GameTextManager::parseStringFile
- Purpose: Parses a text file in string format
- Calls: readLine, removeLeadingAndTrailing, readToEndOfQuote, translateCopy

### compareLUT
- Purpose: Comparison function for sorting string lookup table
- Calls: None

## Globals
- **TheGameText (GameTextInterface*)**: Global text interface instance
- **g_strFile (const Char*)**: Path to string file
- **g_csfFile (const Char*)**: Path to CSF file

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
