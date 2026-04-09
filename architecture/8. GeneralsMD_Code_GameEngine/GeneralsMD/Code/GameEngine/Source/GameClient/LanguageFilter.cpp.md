# GeneralsMD/Code/GameEngine/Source/GameClient/LanguageFilter.cpp

## Purpose
Implements a language filter system to censor profanity or inappropriate words in game chat.

## Responsibilities
- Loads a list of censored words from a file
- Filters text input by replacing censored words with asterisks
- Handles character obfuscation (e.g., "ph" â "f", "1" â "l")
- Provides singleton access via `TheLanguageFilter`

## Key Types
- `LanguageFilter` (Class): Main filter class managing word list and filtering logic
- `None` (Other types are from external headers)

## Key Functions
### `init()`
- Purpose: Loads and decrypts the bad word list from file
- Calls: `TheFileSystem->openFile`, `readWord`, `unHaxor`

### `filterLine()`
- Purpose: Processes a text line, replacing censored words with asterisks
- Calls: `unHaxor`, `m_wordList.find`

### `unHaxor()`
- Purpose: Converts obfuscated characters (e.g., leetspeak) to their base forms
- Calls: None (pure transformation logic)

### `readWord()`
- Purpose: Reads a single word from the bad word file
- Calls: `file1->read`

### `createLanguageFilter()`
- Purpose: Factory function to create a new `LanguageFilter` instance
- Calls: `NEW LanguageFilter`

## Globals
- `TheLanguageFilter` (LanguageFilter*): Singleton instance of the filter
- `ignoredChars` (wchar_t[]): List of characters ignored during filtering

## Dependencies
- `LanguageFilter.h`, `FileSystem.h`, `File.h`
- `UnicodeString`, `File`, `TheFileSystem` (
