# GeneralsMD/Code/GameEngine/Include/GameClient/Water.h

## Purpose
Defines data structures for water and transparency settings in the game, including INI parsing support.

## Responsibilities
- Declares `WaterSetting` class for water appearance properties
- Declares `WaterTransparencySetting` class for transparency and skybox settings
- Provides INI field parsing tables for both classes
- Exposes global instances for runtime access

## Key Types
- **WaterSetting (Class)**: Stores water texture, color, and scrolling properties
- **WaterTransparencySetting (Class)**: Stores transparency, color, and skybox texture settings
- **FieldParse (Struct)**: INI parsing table (external)

## Key Functions
### WaterSetting::getFieldParse
- Purpose: Returns the INI parsing table for water settings
- Calls: None

### WaterTransparencySetting::getFieldParse
- Purpose: Returns the INI parsing table for transparency settings
- Calls: None

## Globals
- **WaterSettings (WaterSetting[])**: Array of water settings per time of day
- **TheWaterTransparency (OVERRIDE<WaterTransparencySetting>)**: Overridable transparency settings

## Dependencies
- `Common/GameType.h`, `Common/Overridable.h`, `Common/Override.h`
- `FieldParse` struct (external)
- `AsciiString`, `RGBAColorInt`, `RGBColor`, `Real`, `Int`, `Bool` types
