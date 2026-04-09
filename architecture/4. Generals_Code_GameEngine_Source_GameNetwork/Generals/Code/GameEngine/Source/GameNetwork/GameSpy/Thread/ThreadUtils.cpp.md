# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/ThreadUtils.cpp

## Purpose
Provides utility functions for character encoding conversion in GameSpy networking.

## Responsibilities
- Converts multi-byte strings to wide-character strings (UTF-8 to UTF-16)
- Converts wide-character strings back to multi-byte strings (UTF-16 to UTF-8)
- Handles newline character normalization in wide strings

## Key Types
- None

## Key Functions
### MultiByteToWideCharSingleLine
- Purpose: Converts a UTF-8 string to a wide-character string while replacing newlines with spaces.
- Calls: `strlen`, `NEW`, `MultiByteToWideChar`, `wcschr`, `wcslen`

### WideCharStringToMultiByte
- Purpose: Converts a wide-character string to a UTF-8 multi-byte string.
- Calls: `WideCharToMultiByte`, `NEW`, `wcslen`

## Globals
- None

## Dependencies
- `<string>` for `std::wstring` and `std::string`
- Windows API functions: `MultiByteToWideChar`, `WideCharToMultiByte`
- `WideChar` type (likely a typedef for `wchar_t`)
- `Int` type (likely a typedef for `int`)
