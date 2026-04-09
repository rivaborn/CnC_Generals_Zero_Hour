# GeneralsMD/Code/GameEngine/Include/Common/urllaunch.h

## Purpose
Header file declaring functions for URL escaping and launching web URLs.

## Responsibilities
- Declares URL escaping function.
- Declares URL launching function.
- Provides interface for web link handling.

## Key Types
- None

## Key Functions
### MakeEscapedURL
- Purpose: Escapes special characters in a URL string.
- Calls: Not inferable

### LaunchURL
- Purpose: Launches the default web browser with the given URL.
- Calls: Not inferable

## Globals
- None

## Dependencies
- Uses `HRESULT` (Windows COM return type).
- Uses `LPWSTR` and `LPCWSTR` (Windows wide string types).
