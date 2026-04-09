# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/urlBuilder.h

## Purpose
Declares a function to construct URLs from registry settings for game updates and patches.

## Responsibilities
- Declares the `FormatURLFromRegistry` function interface
- Provides URL construction logic for game patching
- Handles registry-based URL configuration

## Key Types
- None

## Key Functions
### FormatURLFromRegistry
- Purpose: Constructs URLs from registry settings for game/maps/config/MOTD.
- Calls: Not inferable (implementation in .cpp file)

## Globals
- None

## Dependencies
- `<string>` (std::string)
- Registry access (via external implementation)
- URL construction utilities (via external implementation)
