# GeneralsMD/Code/GameEngine/Source/GameClient/Water.cpp - Enhanced Analysis

## Architectural Role
This file defines the data structures and parsing logic for water rendering settings in the SAGE engine. It bridges the INI configuration system with the rendering pipeline, allowing water properties to be customized per time of day.

## Cross-References
### Incoming
- `INIWater.cpp` calls `parseWaterSettingDefinition` and `parseWaterTransparencyDefinition` (likely via INI parsing infrastructure)
- Other INI parsing modules may reference the `FieldParse` tables for water settings

### Outgoing
- Relies on `Common/INI.h` for parsing utilities and `FieldParse` infrastructure
- Uses `OVERRIDE` template (likely from engine's override system) for global transparency settings

## Design Patterns
- **Data Transfer Object (DTO)**: `WaterSetting` and `WaterTransparencySetting` act as pure data containers for INI configuration
- **Table-Driven Parsing**: Uses `FieldParse` arrays to decouple parsing logic from data structure definitions
- **Singleton-like Global**: `TheWaterTransparency` provides engine-wide access to transparency settings (though not a true singleton)

*Not inferable*: No clear use of Factory, Observer, or other patterns in this snippet.
