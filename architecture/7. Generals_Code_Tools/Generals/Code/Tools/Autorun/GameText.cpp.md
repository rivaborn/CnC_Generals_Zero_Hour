# Generals/Code/Tools/Autorun/GameText.cpp

## Purpose
Manages game text resources, loading and fetching localized strings from .str or .csf files.

## Responsibilities
- Loads and parses string files (autorun.str/autorun.csf)
- Provides string lookup via labels
- Handles missing strings and logging
- Supports both text and speech references

## Key Types
- **StringInfo (struct)**: Stores label, text, and speech for a string entry
- **StringLookUp (struct)**: Lookup table entry mapping label to StringInfo
- **CSFHeader (struct)**: Header structure for CSF binary format files
- **NoString (struct)**: Linked list node for tracking missing strings
- **GameTextManager (class)**: Main text management class implementing GameTextInterface

## Key Functions
### GameTextManager::init
- Purpose: Initializes the text system by loading string files
- Calls: getStringCount, getCSFInfo, parseStringFile, parseCSF, qsort

### GameTextManager::fetch
- Purpose: Retrieves localized string by label
- Calls: bsearch, compareLUT

### GameTextManager::parseCSF
- Purpose: Parses binary CSF format string files
- Calls: file.read, stripSpaces

### GameTextManager::parseStringFile
- Purpose: Parses text-based .str string files
- Calls: readLine, removeLeadingAndTrailing, readToEndOfQuote, translateCopy

### compareLUT
- Purpose: Comparison function for sorting string lookup table
- Calls: stricmp

## Globals
- **TheGameText (GameTextInterface*)**: Global text interface instance
- **szArgvPath (char[])**: Path to executable directory

## Dependencies
- WSYS_File.h, WSYS_RAMFile.h
- std::string, std::wstring
- GameText.h interface
- File I/O and string manipulation functions
