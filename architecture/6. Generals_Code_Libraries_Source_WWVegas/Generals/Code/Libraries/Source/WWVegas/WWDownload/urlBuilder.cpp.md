# Generals/Code/Libraries/Source/WWVegas/WWDownload/urlBuilder.cpp

## Purpose
Constructs download URLs for game updates, maps, config, and MOTD by reading registry values.

## Responsibilities
- Reads SKU, language, version, and map version from registry
- Builds base URL from registry or default
- Formats specific URLs for game patch, map patch, config, and MOTD
- Handles string formatting for URL construction

## Key Types
None

## Key Functions
### FormatURLFromRegistry
- Purpose: Constructs download URLs from registry settings
- Calls: `GetStringFromRegistry`, `GetUnsignedIntFromRegistry`, `_snprintf`

## Globals
None

## Dependencies
- `<string>`, `<stdio.h>`
- `registry.h` (for registry access functions)
