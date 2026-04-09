# Generals/Code/GameEngine/Source/GameClient/Water.cpp

## Purpose
Manages water settings and transparency for the game's water rendering system.

## Responsibilities
- Defines water settings for different times of day
- Parses water-related INI configuration fields
- Initializes default water color and texture properties
- Handles water transparency settings

## Key Types
- **WaterSetting (Class)**: Stores water rendering parameters (textures, colors, scrolling rates)
- **WaterTransparencySetting (Class)**: Stores water transparency and skybox texture settings
- **FieldParse (Struct)**: INI field parsing configuration

## Key Functions
### WaterSetting::WaterSetting()
- Purpose: Initializes default water settings
- Calls: None

### WaterSetting::~WaterSetting()
- Purpose: Destructor for water settings
- Calls: None

## Globals
- **WaterSettings (WaterSetting[])**: Array of water settings for different times of day
- **TheWaterTransparency (OVERRIDE<WaterTransparencySetting>)**: Global water transparency settings

## Dependencies
- "GameClient/Water.h"
- "Common/INI.h"
- INI parsing utilities (parseAsciiString, parseRGBAColorInt, parseReal, parseInt)
