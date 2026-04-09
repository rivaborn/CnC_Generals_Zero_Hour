# GeneralsMD/Code/GameEngine/Include/Common/SkirmishPreferences.h

## Purpose
Defines the `SkirmishPreferences` class for saving/loading skirmish game preferences.

## Responsibilities
- Inherits from `UserPreferences` to extend base user settings.
- Provides methods to get/set skirmish-specific options (slots, faction, color, map, superweapons, starting cash).
- Handles serialization via `write()` method.

## Key Types
- **SkirmishPreferences (Class)**: Manages skirmish game preferences and serialization.

## Key Functions
### SkirmishPreferences()
- Purpose: Constructor for `SkirmishPreferences`.
- Calls: Not inferable.

### ~SkirmishPreferences()
- Purpose: Destructor for `SkirmishPreferences`.
- Calls: Not inferable.

### write()
- Purpose: Serializes skirmish preferences to storage.
- Calls: Not inferable.

### getSlotList()
- Purpose: Retrieves the slot list configuration.
- Calls: Not inferable.

### setSlotList()
- Purpose: Updates the slot list configuration.
- Calls: Not inferable.

### getUserName()
- Purpose: Returns the configured username.
- Calls: Not inferable.

### getPreferredFaction()
- Purpose: Returns the preferred faction ID.
- Calls: Not inferable.

### getPreferredColor()
- Purpose: Returns the preferred player color.
- Calls: Not inferable.

### getPreferredMap()
- Purpose: Returns the preferred map name.
- Calls: Not inferable.

### usesSystemMapDir()
- Purpose: Checks if the system map directory is used.
- Calls: Not inferable.

### getSuperweaponRestricted()
- Purpose: Gets superweapon restriction status.
- Calls: Not inferable.

### setSuperweaponRestricted()
- Purpose: Sets superweapon restriction status.
-
