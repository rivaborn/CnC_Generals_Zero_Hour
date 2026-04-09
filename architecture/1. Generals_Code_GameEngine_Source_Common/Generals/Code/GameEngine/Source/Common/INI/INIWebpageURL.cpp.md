# Generals/Code/GameEngine/Source/Common/INI/INIWebpageURL.cpp

## Purpose
This file contains functions for parsing Webpage URL INI entries and encoding URLs.

## Responsibilities
- Parsing Webpage URL INI entries.
- Encoding URLs to ensure they are valid for web use.

## Key Types
- None

## Key Functions
### encodeURL
- Purpose: Encodes a given URL string by replacing special characters with their hexadecimal representation.
- Calls: 
  - `AsciiString::isEmpty()`
  - `AsciiString::concat()`
  - `AsciiString::find()`
  - `AsciiString::format()`

### parseWebpageURLDefinition
- Purpose: Parses Webpage URL definitions from an INI file and updates the WebBrowser with the parsed URLs.
- Calls:
  - `INI::getNextToken()`
  - `WebBrowser::findURL()`
  - `WebBrowser::makeNewURL()`
  - `AsciiString::startsWith()`
  - `getcwd()`
  - `GetRegistryLanguage()`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/INI.h"
  - "Common/Registry.h"
  - "GameNetwork/WOLBrowser/WebBrowser.h"
