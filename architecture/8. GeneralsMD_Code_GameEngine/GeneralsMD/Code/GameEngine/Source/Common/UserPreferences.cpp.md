# GeneralsMD/Code/GameEngine/Source/Common/UserPreferences.cpp

## Purpose
Handles saving and loading user preferences for the game, including quick match, custom match, ladder, and ignore settings.

## Responsibilities
- Load and save preference data from/to INI files
- Manage preference keys and values (booleans, integers, strings, reals)
- Support specialized preference classes (QuickMatchPreferences, CustomMatchPreferences, etc.)
- Convert data types to/from string representations
- Handle GameSpy-related preferences

## Key Types
- **UserPreferences (Class)**: Base class for preference management
- **QuickMatchPreferences (Class)**: Quick match settings (maps, points, ping limits)
- **CustomMatchPreferences (Class)**: Custom match settings (superweapons, factions, stats)
- **GameSpyMiscPreferences (Class)**: GameSpy-specific preferences (locale, cached stats)
- **IgnorePreferences (Class)**: Player ignore list management
- **LadderPreferences (Class)**: Ladder game preferences and history

## Key Functions
### `load`
- Purpose: Load preferences from an INI file
- Calls: `fopen`, `fgets`, `find`, `operator[]`

### `write`
- Purpose: Save preferences to an INI file
- Calls: `fopen`, `fprintf`, `begin`, `end`

### `getBool`/`setBool`
- Purpose: Get/set boolean preferences
- Calls: `getAsciiString`, `boolAsStr`

### `getInt`/`setInt`
- Purpose: Get/set integer preferences
- Calls: `getAsciiString`, `intAsStr`

### `getReal`/`setReal`
- Purpose: Get/set floating-point preferences
- Calls: `getAsciiString`, `realAsStr`

## Globals
- **superweaponRestrictionKey (const char[])**: Key for superweapon restriction preference
- **startingCashKey (const char[])**: Key for starting cash preference
- **limitFactionsKey (const char[])**: Key for faction limitation preference
- **useStatsKey (const char[])**: Key for stats usage preference

## Dependencies
- `PreRTS.h`, `UserPreferences.h`, `Registry.h`, `QuotedPrintable.h`
- `GameSpyMiscPreferences.h`, `LadderPreferences.h`, `Player.h`
- `QuickmatchPreferences.h`, `CustomMatchPreferences.h`, `IgnorePreferences.h`
- `MultiplayerSettings.h`, `MapUtil.h`, `ChallengeGenerals.h`, `PeerDefs.h`
