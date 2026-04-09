# GeneralsMD/Code/GameEngine/Include/Common/GameSpyMiscPreferences.h

## Purpose
Defines the `GameSpyMiscPreferences` class for saving/loading miscellaneous GameSpy-related preferences.

## Responsibilities
- Manage GameSpy-specific user preferences
- Provide accessors for locale, cached stats, quick match resolution lock, and max messages per update
- Inherit from `UserPreferences` base class

## Key Types
- **GameSpyMiscPreferences (Class)**: Handles GameSpy misc preferences storage and retrieval

## Key Functions
### `GameSpyMiscPreferences()`
- Purpose: Default constructor
- Calls: None

### `~GameSpyMiscPreferences()`
- Purpose: Virtual destructor
- Calls: None

### `getLocale()`
- Purpose: Returns the current locale setting
- Calls: None

### `setLocale(Int val)`
- Purpose: Sets the locale preference
- Calls: None

### `getCachedStats()`
- Purpose: Returns cached GameSpy stats as string
- Calls: None

### `setCachedStats(AsciiString val)`
- Purpose: Sets cached GameSpy stats
- Calls: None

### `getQuickMatchResLocked()`
- Purpose: Checks if quick match resolution is locked
- Calls: None

### `getMaxMessagesPerUpdate()`
- Purpose: Returns max messages per update limit
- Calls: None

## Globals
- None

## Dependencies
- `UserPreferences.h` (base class)
- `AsciiString` (string type)
- `Int`, `Bool` (primitive types)
