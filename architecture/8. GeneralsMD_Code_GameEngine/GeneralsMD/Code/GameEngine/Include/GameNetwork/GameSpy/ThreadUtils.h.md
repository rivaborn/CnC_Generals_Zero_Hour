# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/ThreadUtils.h

## Purpose
Header file declaring utility functions for character encoding conversion in GameSpy networking.

## Responsibilities
- Declares string conversion functions for multi-byte to wide-char and vice versa.
- Provides single-line conversion utilities for GameSpy thread operations.
- Ensures proper encoding handling for network communication.

## Key Types
None

## Key Functions
### MultiByteToWideCharSingleLine
- Purpose: Converts a multi-byte string to a wide-character string for single-line input.
- Calls: Not inferable

### WideCharStringToMultiByte
- Purpose: Converts a wide-character string back to a multi-byte string.
- Calls: Not inferable

## Globals
None

## Dependencies
- `<string>` (for `std::wstring` and `std::string`)
- `WideChar` (custom type, not defined here)
