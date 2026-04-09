# GeneralsMD/Code/GameEngine/Include/GameClient/Snow.h

## Purpose
Defines classes for managing snow weather effects in the game, including settings and rendering control.

## Responsibilities
- Define snow weather settings (transparency, vertex settings)
- Manage snow particle system (position, velocity, rendering)
- Provide INI parsing for snow configuration
- Control visibility of snow effects

## Key Types
- **WeatherSetting (Class)**: Holds snow effect parameters (texture, frequency, amplitude, etc.)
- **WeatherSettingMagicEnum (Enum)**: Not inferable (likely internal glue code)
- **WeatherSetting_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal glue code)
- **SnowManager (Class)**: Manages snow particle system rendering and updates
- **(anonymous enum) (Enum)**: Defines noise table dimensions (SNOW_NOISE_X, SNOW_NOISE_Y)

## Key Functions
### WeatherSetting::WeatherSetting
- Purpose: Initializes default snow settings (texture, frequencies, velocities, etc.)
- Calls: None

### SnowManager::init
- Purpose: Initializes snow manager state
- Calls: Not inferable

### SnowManager::updateIniSettings
- Purpose: Updates snow settings from INI configuration
- Calls: Not inferable

### SnowManager::setVisible
- Purpose: Enables/disables snow rendering
- Calls: Not inferable

## Globals
- **TheWeatherSetting (OVERRIDE<WeatherSetting>)**: Global weather settings instance
- **TheSnowManager (SnowManager*)**: Global snow manager singleton

## Dependencies
- `Lib/BaseType.h`, `Common/SubsystemInterface.h`, `Common/Overridable.h`, `Common/Override.h`
- `WWMATH/Vector3.h`, `WWMATH/Vector4.h`
- Uses `Overridable`
