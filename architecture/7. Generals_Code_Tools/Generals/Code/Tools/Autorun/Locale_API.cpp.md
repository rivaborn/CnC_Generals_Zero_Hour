# Generals/Code/Tools/Autorun/Locale_API.cpp

## Purpose
Handles localization and string retrieval for the game's autorun tool, supporting multiple languages and code pages.

## Responsibilities
- Initializes and manages locale resources
- Retrieves localized strings in both char and wchar_t formats
- Handles multi-language file formats (configurable)
- Removes quotes from localized strings
- Manages game text interface

## Key Types
- **None**

## Key Functions
### Remove_Quotes_Around_String
- Purpose: Removes surrounding quotes from a string
- Calls: None

### Locale_Use_Multi_Language_Files
- Purpose: Returns whether multi-language file format is enabled
- Calls: None

### Locale_Init
- Purpose: Initializes the locale system with specified language and file
- Calls: CreateGameTextInterface, TheGameText->init, LOCALE_init, LOCALE_setbank, LOCALE_loadtable, Load_File

### Locale_Restore
- Purpose: Cleans up locale resources
- Calls: TheGameText->delete, LOCALE_freetable, LOCALE_restore, free

### Locale_GetString (char version)
- Purpose: Retrieves a localized string and converts it to char format
- Calls: LOCALE_getstring, LOCALE_getstr, Remove_Quotes_Around_String, WideCharToMultiByte

### Locale_GetString (wchar_t version)
- Purpose: Retrieves a localized string using GameText interface
- Calls: TheGameText->fetch

## Globals
- **localeStringsMissing** (wchar_t*): Array of fallback strings for missing translations
- **LanguageFile** (char): Path to language file
- **LocaleFile** (void*): Handle to loaded locale data
- **CodePage** (int): Current code page (default: GetACP())
- **LanguageID** (int): Current language ID
- **PrimaryLanguage** (int): Primary language identifier
- **SubLanguage** (int): Sub-language identifier

## Dependencies
- Key includes: locale.h, locale_api.h, utils.h, wnd_file.h, GameText.h
- External symbols: CreateGameTextInterface, LOCALE_init, LOCALE_setbank, LOCALE_loadtable, LOCALE_getstring, LOCALE_getstr, LOCALE_freetable, LOCALE_restore, Load_File, GetACP, FindResourceEx, LoadResource, SizeofResource, UnlockResource, FreeResource, WideCharToMultiByte, GetModuleHandle, MAKELANGID
