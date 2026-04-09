# Generals/Code/Tools/WorldBuilder/src/MapSettings.cpp

## Purpose
Handles the map settings dialog in WorldBuilder, allowing users to configure time of day, weather, map title, and compression settings.

## Responsibilities
- Populates and manages UI controls for map settings
- Updates global data and world dictionary with user selections
- Handles event callbacks for UI changes

## Key Types
- **MapSettings (class)**: Dialog class for map settings UI
- **TimeOfDay (enum)**: Time of day options
- **Weather (enum)**: Weather options
- **CompressionType (enum)**: Compression algorithm types

## Key Functions
### MapSettings::OnInitDialog
- Purpose: Initializes dialog controls with current settings
- Calls: `GetDlgItem`, `ResetContent`, `AddString`, `SetCurSel`, `getWorldDict`, `getAsciiString`, `getInt`, `getCompressionNameByType`, `getPreferredCompression`

### MapSettings::OnOK
- Purpose: Saves user selections to global data and world dictionary
- Calls: `GetDlgItem`, `GetCurSel`, `setTimeOfDay`, `setAsciiString`, `setInt`

### MapSettings::OnChangeMapTimeofday / OnChangeMapWeather / OnChangeMapCompression / OnChangeMapTitle
- Purpose: Event handlers for UI changes (mostly empty implementations)
- Calls: None

## Globals
- **TheGlobalData (GlobalData)**: Accesses current game settings
- **TheWritableGlobalData (GlobalData)**: Modifies game settings
- **TimeOfDayNames (const char**)**: Array of time of day names
- **WeatherNames (const char**)**: Array of weather names

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `MapSettings.h`, `Common\GlobalData.h`, `Common
