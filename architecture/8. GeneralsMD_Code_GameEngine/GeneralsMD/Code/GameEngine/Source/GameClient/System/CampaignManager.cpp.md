# GeneralsMD/Code/GameEngine/Source/GameClient/System/CampaignManager.cpp

## Purpose
Manages campaign flow, missions, and game state persistence in Command & Conquer Generals Zero Hour.

## Responsibilities
- Loads and parses campaign data from INI files
- Tracks current campaign/mission state
- Handles mission transitions and progression
- Serializes/deserializes campaign state for save/load
- Manages challenge campaign-specific data

## Key Types
- **CampaignManager (Class)**: Singleton managing campaign state and flow
- **Campaign (Class)**: Represents a campaign with missions and metadata
- **Mission (Class)**: Represents individual missions with maps, objectives, etc.
- **Difficulty (Enum)**: Game difficulty levels (e.g., DIFFICULTY_NORMAL)

## Key Functions
### `parseCampaignDefinition`
- Purpose: Parses campaign definitions from INI files
- Calls: `newCampaign`, `initFromINI`

### `gotoNextMission`
- Purpose: Advances to the next mission in the current campaign
- Calls: `getNextMission`

### `xfer`
- Purpose: Serializes/deserializes campaign state for save/load
- Calls: `setCampaignAndMission`, `xferSnapshot`, `xferVersion`

### `parseMissionPart`
- Purpose: Parses mission-specific data from INI files
- Calls: `newMission`, `initFromINI`

## Globals
- **TheCampaignManager (CampaignManager\*)**: Singleton instance of CampaignManager

## Dependencies
- `INI.h`, `Xfer.h`, `GameClient.h`, `GameInfo.h`
- `AsciiString`, `FieldParse`, `Xfer`, `SkirmishGameInfo`
