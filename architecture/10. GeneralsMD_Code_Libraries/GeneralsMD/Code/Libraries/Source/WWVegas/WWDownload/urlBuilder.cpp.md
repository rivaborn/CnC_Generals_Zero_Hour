# GeneralsMD/Code/Libraries/Source/WWVegas/WWDownload/urlBuilder.cpp

## Purpose
Constructs patch and configuration URLs from registry settings for Generals Zero Hour.

## Responsibilities
- Reads SKU, language, version, and map version from registry
- Builds URLs for game patches, map patches, config, and MOTD
- Uses base URL from registry or default fallback

## Key Types
None

## Key Functions
### FormatURLFromRegistry
- Purpose: Constructs patch and config URLs from registry values
- Calls: GetStringFromRegistry, GetUnsignedIntFromRegistry

## Globals
None

## Dependencies
- `<string>`, `<stdio.h>`
- `registry.h` (GetStringFromRegistry, GetUnsignedIntFromRegistry)
