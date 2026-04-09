# GeneralsMD/Code/GameEngine/Include/Common/SkirmishPreferences.h - Enhanced Analysis

## Architectural Role
This header defines the `SkirmishPreferences` class, which extends the base `UserPreferences` to manage skirmish-specific game settings. It bridges the user configuration system with the skirmish game mode, handling serialization and convenience accessors for faction, color, map, and superweapon preferences.

## Cross-References
### Incoming
- Likely called by skirmish game mode initialization (e.g., `SkirmishGame.cpp`)
- Used by UI components for preference editing (e.g., `SkirmishOptionsDialog.cpp`)
- Referenced in save/load systems for game state persistence

### Outgoing
- Inherits from `UserPreferences`, relying on its base serialization mechanisms
- Uses `AsciiString` and `UnicodeString` for string handling (from `Common` utilities)
- Interacts with map directory resolution systems (via `usesSystemMapDir()`)

## Design Patterns
- **Template Method**: The `write()` method suggests a template method pattern where base class handles serialization, and derived class provides data.
- **Facade**: Acts as a facade for skirmish-specific preferences, simplifying access to complex user settings.
- **Property**: Uses getter/setter pairs (e.g., `getSuperweaponRestricted()`/`setSuperweaponRestricted()`) for encapsulated attribute access.
