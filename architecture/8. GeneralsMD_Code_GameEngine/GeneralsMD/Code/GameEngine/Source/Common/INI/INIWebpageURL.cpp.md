# GeneralsMD/Code/GameEngine/Source/Common/INI/INIWebpageURL.cpp

## Purpose
Handles parsing of webpage URL entries from INI files and URL encoding.

## Responsibilities
- Parses INI entries for webpage URLs
- Encodes URLs using percent-encoding
- Modifies file:// URLs to include game data paths

## Key Types
- None

## Key Functions
### encodeURL
- Purpose: Encodes a string into URL-safe format using percent-encoding
- Calls: AsciiString::isEmpty(), AsciiString::concat(), AsciiString::format(), isalnum(), AsciiString::find()

### INI::parseWebpageURLDefinition
- Purpose: Parses INI entries for webpage URLs and initializes WebBrowserURL objects
- Calls: INI::getNextToken(), WebBrowser::findURL(), WebBrowser::makeNewURL(), INI::initFromINI(), WebBrowserURL::getFieldParse(), encodeURL(), getcwd(), GetRegistryLanguage()

## Globals
- None

## Dependencies
- PreRTS.h
- Common/INI.h
- Common/Registry.h
- GameNetwork/WOLBrowser/WebBrowser.h
- AsciiString class
- WebBrowserURL class
- WebBrowser singleton (TheWebBrowser)
