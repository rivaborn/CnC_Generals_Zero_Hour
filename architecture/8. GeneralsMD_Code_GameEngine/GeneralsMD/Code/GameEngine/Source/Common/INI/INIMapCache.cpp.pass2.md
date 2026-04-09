# GeneralsMD/Code/GameEngine/Source/Common/INI/INIMapCache.cpp - Enhanced Analysis

## Architectural Role
This file is part of the INI parsing subsystem, specifically handling map metadata deserialization. It bridges the INI configuration system with the game's map loading infrastructure, enabling runtime map discovery and metadata access.

## Cross-References
### Incoming
- Likely called by the map loading system during initialization or when scanning for available maps
- May be invoked by the UI when displaying the map selection screen

### Outgoing
- Uses `INI` class for parsing functionality
- Depends on `MapUtil.h` for map metadata structures
- Interacts with `GameText` for localized map names
- Accesses `TheMapCache` global for storing parsed map data

## Design Patterns
- **Parser Pattern**: Uses a field parse table to define how INI entries map to class members
- **Adapter Pattern**: Converts INI data into internal `MapMetaData` structures
- **Singleton Access**: Relies on global singletons (`TheMapCache`, `TheGameText`) for system-wide data access

Rules followed. Output under 400 tokens.
