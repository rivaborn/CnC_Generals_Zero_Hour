# Generals/Code/GameEngine/Source/GameClient/LanguageFilter.cpp

## Purpose
Manages a language filter system to censor profanity or inappropriate words in game chat.

## Responsibilities
- Loads and manages a list of censored words from a file
- Filters text input by replacing censored words with asterisks
- Handles character obfuscation (e.g., "ph" â "f", "1" â "l")
- Provides singleton-like access via global instance

## Key Types
- `LanguageFilter` (Class): Main filter class managing word list and filtering logic
- `None` (Other types are standard or from dependencies)

## Key Functions
### `init`
- Purpose: Loads censored words from file and initializes the filter
- Calls: `TheFileSystem->openFile`, `readWord`, `unHaxor`

### `filterLine`
- Purpose: Processes a text line, replacing censored words with asterisks
- Calls: `unHaxor`, `m_wordList.find`

### `unHaxor`
- Purpose: Decodes obfuscated characters in words (e.g., leetspeak)
- Calls: None (pure logic)

### `readWord`
- Purpose: Reads a single word from the file (internal helper)
- Calls: `file1->read`

### `createLanguageFilter`
- Purpose: Factory function to create a new `LanguageFilter` instance
- Calls: None

## Globals
- `TheLanguageFilter` (LanguageFilter*): Global singleton instance of the filter
- `ignoredChars` (wchar_t[]): List of characters ignored during filtering

## Dependencies
- `GameClient/LanguageFilter.h` (header)
- `Common/FileSystem.h`, `Common/File.h` (file I/O)
- `PreRTS.h` (
