# GeneralsMD/Code/GameEngine/Source/GameClient/Water.cpp

## Purpose
Manages water settings and transparency configurations for the game's water rendering system.

## Responsibilities
- Defines water settings for different times of day
- Parses water-related INI configuration fields
- Initializes default water and transparency settings
- Provides field parsing tables for INI configuration

## Key Types
- **WaterSetting (Class)**: Stores water rendering parameters (textures, colors, scrolling rates)
- **WaterTransparencySetting (Class)**: Stores water transparency and skybox settings
- **FieldParse arrays**: Define INI parsing rules for water settings

## Key Functions
### WaterSetting::WaterSetting()
- Purpose: Initializes water settings with default values
- Calls: None

### WaterSetting::~WaterSetting()
- Purpose: Destructor for water settings
- Calls: None

## Globals
- **WaterSettings (WaterSetting[])**: Array of water settings for different times of day
- **TheWaterTransparency (OVERRIDE<WaterTransparencySetting>)**: Global water transparency settings

## Dependencies
- "PreRTS.h", "GameClient/Water.h", "Common/INI.h"
- INI parsing utilities (INI::parseAsciiString, INI::parseRGBAColorInt, etc.)
- FieldParse structure for INI configuration parsing
