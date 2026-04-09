# Generals/Code/Tools/Autorun/Locale_API.h

## Purpose
Header file defining the locale API for internationalization support in the game.

## Responsibilities
- Declares global variables for locale management
- Provides function prototypes for locale initialization, restoration, and string retrieval
- Supports multi-language file handling

## Key Types
None

## Key Functions
### Locale_Init
- Purpose: Initialize the locale system with a specific language and file.
- Calls: Not inferable

### Locale_Restore
- Purpose: Restore the original locale settings.
- Calls: Not inferable

### Locale_GetString
- Purpose: Retrieve a localized string by its ID.
- Calls: Not inferable

### Locale_Use_Multi_Language_Files
- Purpose: Check if multi-language file support is enabled.
- Calls: Not inferable

## Globals
- CodePage (int): Stores the current code page for character encoding.
- LocaleFile (void*): Pointer to the loaded locale file.
- LanguageID (int): Identifier for the current language.
- LanguageFile (char[]): Name of the language file.
- PrimaryLanguage (int): Primary language identifier.
- SubLanguage (int): Sub-language identifier.

## Dependencies
- `<STDLIB.H>`: For standard library functions and macros.
- `_MAX_PATH`: Macro for maximum path length (from Windows API).
