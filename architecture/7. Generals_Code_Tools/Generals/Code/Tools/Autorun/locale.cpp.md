# Generals/Code/Tools/Autorun/locale.cpp

## Purpose
Handles localization (string loading and retrieval) for the game, supporting multiple languages via .loc files.

## Responsibilities
- Load and parse locale files (.loc format)
- Manage multiple language banks
- Provide string lookup by ID
- Memory management for loaded strings

## Key Types
- LOCALEFILE_HEADERCHUNK (Class): Header structure for locale files
- LOCALEFILE_INDEXCHUNK (Class): Index structure mapping string IDs to offsets
- LOCALEFILE_LANGUAGECHUNK (Class): Language-specific string data container
- LOCALE_INSTANCE (Class): Main locale system state tracker

## Key Functions
### LOCALE_init
- Purpose: Initialize the locale system
- Calls: galloc, memset

### LOCALE_loadtable
- Purpose: Load a locale table from a file
- Calls: gopen, readheader, readstrings, gclose

### LOCALE_getstring
- Purpose: Retrieve a string by its ID from the current bank
- Calls: getstringbyindex, bsearch

### LOCALE_freetable
- Purpose: Free resources used by the current bank
- Calls: gfree

## Globals
- lx (LOCALE_INSTANCE*): Main locale system instance
- LOCALElanguageid (int): Current language ID

## Dependencies
- gimex.h (file/memory I/O)
- locale.h (locale definitions)
- wnd_file.h (file operations)
- string.h (memory operations)
- assert.h (assertions)
