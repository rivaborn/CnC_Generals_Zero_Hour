# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/ThreadUtils.cpp

## Purpose
Provides utility functions for character encoding conversion in GameSpy networking.

## Responsibilities
- Converts multi-byte strings to wide-character strings (UTF-8 to UTF-16)
- Converts wide-character strings back to multi-byte strings (UTF-16 to UTF-8)
- Removes newline characters during conversion

## Key Types
- None

## Key Functions
### MultiByteToWideCharSingleLine
- Purpose: Converts a UTF-8 string to UTF-16, replacing newlines with spaces.
- Calls: `strlen`, `NEW`, `MultiByteToWideChar`, `wcschr`, `wcslen`

### WideCharStringToMultiByte
- Purpose: Converts a UTF-16 string back to UTF-8.
- Calls: `WideCharToMultiByte`, `NEW`, `wcslen`

## Globals
- None

## Dependencies
- `<string>` (std::wstring, std::string)
- `<cstring>` (strlen)
- Windows API: `MultiByteToWideChar`, `WideCharToMultiByte`, `wcschr`, `wcslen`
- Custom types: `WideChar`, `Int`
- Memory allocation: `NEW` (custom allocator)
