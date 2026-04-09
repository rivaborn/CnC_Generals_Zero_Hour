# Generals/Code/Tools/WorldBuilder/src/playerlistdlg.cpp

## Purpose
Manages player list UI and player configuration in WorldBuilder, including alliances, factions, and team settings.

## Responsibilities
- Player creation, editing, and removal
- Alliance/enemy relationship management
- Player faction and color selection
- UI synchronization with player data

## Key Types
- **PlayerListDlg (Class)**: Main dialog class for player management
- **SidesList (Class)**: Player/team data container
- **Dict (Class)**: Player attribute storage

## Key Functions
### `islegalplayernamechar`
- Purpose: Validates player name characters
- Calls: `::isalnum`

### `fixDefaultTeamName`
- Purpose: Updates team names when player names change
- Calls: `sides.findTeamInfo`, `Dict::setAsciiString`

### `updateAllTeams`
- Purpose: Updates team ownership references
- Calls: `sides.getTeamInfo`, `Dict::getAsciiString`, `Dict::setAsciiString`

### `ensureValidPlayerName`
- Purpose: Sanitizes player names by replacing invalid characters
- Calls: `Dict::getAsciiString`, `Dict::setAsciiString`

### `calcRelationStr`
- Purpose: Determines relationship between players
- Calls: `sides.getSideInfo`, `Dict::getAsciiString`, `containsToken`

## Globals
- **NEUTRAL_NAME_STR (const char*)**: Neutral player name constant
- **thePrevCurPlyr (Int)**: Remembers last selected player index

## Dependencies
- `worldbuilder.h`, `playerlistdlg.h`, `MapObjectProps.h`
- `Common/WellKnownKeys.h`, `Common/PlayerTemplate.h`
- `GameLogic/SidesList.h`, `GameClient/GameText.h`
- MFC classes (`CDialog`, `CListBox`, etc.)
