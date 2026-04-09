# Generals/Code/GameEngine/Source/Common/System/SaveGame/GameStateMap.cpp

## Purpose
This file handles the embedding and extraction of map data into/from save game files in Command & Conquer Generals.

## Responsibilities
- Embeds pristine or in-use maps into save game files.
- Extracts maps from save game files to temporary locations.
- Manages scratch pad maps in the save directory.
- Handles versioning for saved game data.

## Key Types
- None

## Key Functions
### embedPristineMap
- Purpose: Embeds a pristine map file into the xfer stream.
- Calls: `TheFileSystem->openFile`, `file->seek`, `file->read`, `xfer->beginBlock`, `xfer->xferUser`, `xfer->endBlock`.

### embedInUseMap
- Purpose: Embeds an in-use map from a temporary file into the xfer stream.
- Calls: `fopen`, `fseek`, `ftell`, `fread`, `xfer->beginBlock`, `xfer->xferUser`, `xfer->endBlock`.

### extractAndSaveMap
- Purpose: Extracts map data from the xfer stream and saves it to a file.
- Calls: `fopen`, `fwrite`, `xfer->beginBlock`, `xfer->xferUser`, `xfer->endBlock`.

### GameStateMap::xfer
- Purpose: Handles the transfer of game state, including map data, between save files.
- Calls: `embedPristineMap`, `embedInUseMap`, `extractAndSaveMap`, `TheGameLogic->getGameMode`, `TheGameLogic->setGameMode`, `TheGameLogic->startNewGame`.

## Globals
- TheGameStateMap (GameStateMap*): Pointer to the game state map instance.

## Dependencies
- Key includes: "Common/File.h", "Common/FileSystem.h", "Common/GameState.h", "Common/GameStateMap.h", "Common/GlobalData.h", "Common/Xfer.h", "GameClient/GameClient.h", "GameLogic/GameLogic.h".
- External symbols: `TheFileSystem`, `TheGameState`, `TheGlobalData`, `TheWritableGlobalData`, `TheGameLogic`, `TheGameClient`, `SC_INVALID_DATA`.
