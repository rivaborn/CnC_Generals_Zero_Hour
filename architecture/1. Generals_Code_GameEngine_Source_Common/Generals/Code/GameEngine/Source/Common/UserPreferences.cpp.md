# Generals/Code/GameEngine/Source/Common/UserPreferences.cpp

## Purpose
Handles loading and saving user preferences, including various settings for QuickMatch, CustomMatch, GameSpyMisc, Ignore, and Ladder preferences.

## Responsibilities
- Load and save user preferences from/to files.
- Convert between different data types (int, bool, real) and their string representations.
- Manage specific preference categories like QuickMatch, CustomMatch, etc.

## Key Types
- `UserPreferences` (Class): Manages general user preferences.
- `QuickMatchPreferences` (Class): Manages quick match settings.
- `CustomMatchPreferences` (Class): Manages custom match settings.
- `GameSpyMiscPreferences` (Class): Manages miscellaneous GameSpy settings.
- `IgnorePreferences` (Class): Manages ignored users.
- `LadderPreferences` (Class): Manages ladder preferences.

## Key Functions
### load
- Purpose: Loads user preferences from a file.
- Calls: `fopen`, `fgets`, `fclose`

### write
- Purpose: Writes user preferences to a file.
- Calls: `fopen`, `fprintf`, `fclose`

### getBool, getInt, getReal, getAsciiString
- Purpose: Retrieve preference values with default options.
- Calls: `atoi`, `atof`, `stricmp`

### setBool, setInt, setReal, setAsciiString
- Purpose: Set preference values.
- Calls: `intAsStr`, `boolAsStr`, `realAsStr`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/GameSpyMiscPreferences.h"
  - "Common/UserPreferences.h"
  - "Common/LadderPreferences.h"
  - "Common/Player.h"
  - "Common/PlayerTemplate.h"
  - "Common/Registry.h"
  - "Common/QuickmatchPreferences.h"
  - "Common/CustomMatchPreferences.h"
  - "Common/IgnorePreferences.h"
  - "Common/QuotedPrintable.h"
  - "Common/MultiplayerSettings.h"
  - "GameClient/MapUtil.h"
  - "GameNetwork/GameSpy/PeerDefs.h"

- External symbols used:
  - `TheGlobalData`
  - `TheGameSpyInfo`
  - `TheMultiplayerSettings`
  - `ThePlayerTemplateStore`
