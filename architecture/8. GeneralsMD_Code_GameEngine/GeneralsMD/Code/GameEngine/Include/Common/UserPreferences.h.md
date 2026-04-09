# GeneralsMD/Code/GameEngine/Include/Common/UserPreferences.h

## Purpose
Defines classes for managing user preferences, including game options, LAN settings, and preference storage.

## Responsibilities
- Provides base class for preference storage (UserPreferences)
- Manages game options (OptionPreferences)
- Handles LAN-specific preferences (LANPreferences)
- Supports loading/saving preferences to/from files

## Key Types
- **Money (Class)**: Not inferable.
- **PreferenceMap (Class)**: Typedef for map of string preferences.
- **UserPreferences (Class)**: Base class for preference storage.
- **OptionPreferences (Class)**: Manages game options and settings.
- **LANPreferences (Class)**: Manages LAN-specific preferences.

## Key Functions
### UserPreferences::load
- Purpose: Load preferences from file.
- Calls: Not inferable.

### UserPreferences::write
- Purpose: Write preferences to file.
- Calls: Not inferable.

### OptionPreferences::getLANIPAddress
- Purpose: Get LAN IP address.
- Calls: Not inferable.

### LANPreferences::getUserName
- Purpose: Get user name for LAN.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- "Common/STLTypedefs.h"
- Money class (forward declared)
- STL map, string types
