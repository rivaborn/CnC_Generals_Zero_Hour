# Generals/Code/Tools/Autorun/locale.h

## Purpose
Header file defining the LOCALE API for string localization in the game.

## Responsibilities
- Declares functions for loading, managing, and retrieving localized strings.
- Provides both a modern simplified API and an obsolete backward-compatible API.
- Defines constants for locale bank management.

## Key Types
None

## Key Functions
### LOCALE_getstr
- Purpose: Retrieves a localized string from a locale file.
- Calls: Not inferable

### LOCALE_init
- Purpose: Initializes the locale system.
- Calls: Not inferable

### LOCALE_restore
- Purpose: Frees all resources allocated by the locale system.
- Calls: Not inferable

### LOCALE_setbank
- Purpose: Sets the current locale bank.
- Calls: Not inferable

### LOCALE_getbank
- Purpose: Returns the current locale bank ID.
- Calls: Not inferable

### LOCALE_getbanklanguageid
- Purpose: Returns the language ID of the current locale bank.
- Calls: Not inferable

### LOCALE_getbankstringcount
- Purpose: Returns the number of strings in the current locale bank.
- Calls: Not inferable

### LOCALE_loadtable
- Purpose: Loads a locale table into the current bank.
- Calls: Not inferable

### LOCALE_freetable
- Purpose: Frees the locale table in the current bank.
- Calls: Not inferable

### LOCALE_getstring
- Purpose: Retrieves a localized string using an ID.
- Calls: Not inferable

## Globals
None

## Dependencies
- Not inferable
