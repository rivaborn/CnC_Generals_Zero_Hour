# GeneralsMD/Code/GameEngine/Source/GameClient/Snow.cpp

## Purpose
Implements snow rendering effects in the game using particle systems.

## Responsibilities
- Manages snow particle generation and rendering
- Handles snow visibility and configuration
- Parses snow-related settings from INI files
- Updates snow particle positions over time

## Key Types
- **SnowManager (Class)**: Manages snow particle system
- **WeatherSetting (Class)**: Contains snow effect parameters
- **TheSnowManager (Global)**: Singleton instance of SnowManager
- **TheWeatherSetting (Global)**: Singleton instance of WeatherSetting

## Key Functions
### `SnowManager::init`
- Purpose: Initializes snow particle system
- Calls: `updateIniSettings`

### `SnowManager::updateIniSettings`
- Purpose: Updates snow parameters from INI settings
- Calls: None

### `INI::parseWeatherDefinition`
- Purpose: Parses weather settings from INI file
- Calls: `WeatherSetting::initFromINI`, `TheSnowManager->updateIniSettings`

## Globals
- **TheSnowManager (SnowManager*)**: Global snow manager instance
- **TheWeatherSetting (WeatherSetting*)**: Global weather settings instance

## Dependencies
- `GameClient/Snow.h`
- `GameClient/view.h`
- `PreRTS.h`
- INI parsing system
- Memory allocation functions
