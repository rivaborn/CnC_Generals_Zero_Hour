# GeneralsMD/Code/GameEngine/Source/Common/System/SaveGame/GameStateMap.cpp

## Purpose
Handles saving and loading map data in save game files for Command & Conquer Generals Zero Hour.

## Responsibilities
- Embeds pristine or in-use map files into save game streams
- Extracts map data from save game streams
- Manages temporary scratch pad maps in the save directory
- Transfers game state counters (object IDs, drawable IDs) during save/load
- Handles cross-machine compatibility for map paths

## Key Types
- **GameStateMap (Class)**: Manages map data serialization in save games
- **SaveGameInfo (External)**: Contains save game metadata (not defined here)

## Key Functions
### embedPristineMap
- Purpose: Embeds a pristine map file into the save game stream
- Calls: `TheFileSystem->openFile`, `xfer->beginBlock`, `xfer->xferUser`, `xfer->endBlock`

### embedInUseMap
- Purpose: Embeds a previously extracted map file into the save game stream
- Calls: `fopen`, `fseek`, `ftell`, `fread`, `xfer->beginBlock`, `xfer->xferUser`, `xfer->endBlock`

### extractAndSaveMap
- Purpose: Extracts map data from the save game stream and saves it as a temporary file
- Calls: `fopen`, `xfer->beginBlock`, `xfer->xferUser`, `xfer->endBlock`

### clearScratchPadMaps
- Purpose: Deletes temporary map files from the save directory
- Calls: `GetCurrentDirectory`, `SetCurrentDirectory`, `FindFirstFile`, `FindNextFile`, `DeleteFile`, `FindClose`

## Globals
- **TheGameStateMap (GameStateMap*)**: Singleton instance of the GameStateMap class

## Dependencies
- Key includes: `Common/File.h`, `Common/GameState.h`, `Common/Xfer.h`, `GameClient/CampaignManager.h`
- External symbols: `TheFileSystem`, `TheGameState`, `TheGlobalData`, `TheGameLogic`, `TheGameClient`, `TheSkirmishGameInfo`
