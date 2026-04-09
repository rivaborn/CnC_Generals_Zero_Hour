# Generals/Code/GameEngine/Source/GameClient/GameClient.cpp

## Purpose
Implements the GameClient singleton, managing client-side game state, rendering, and user input.

## Responsibilities
- Manages drawables, translators, and game UI components
- Handles serialization/deserialization of game state
- Coordinates input and display systems
- Maintains game frame timing

## Key Types
- `GameClient` (Class): Main client manager singleton
- `DrawableTOCEntry` (Struct): Table of contents entry for drawables
- `shouldSaveDrawable` (Function): Determines if a drawable should be saved

## Key Functions
### `shouldSaveDrawable`
- Purpose: Checks if a drawable should be saved based on its status and object attachment
- Calls: `testDrawableStatus`, `getObject`

### `xferDrawableTOC`
- Purpose: Serializes/deserializes the drawable table of contents
- Calls: `findTOCEntryByName`, `addTOCEntry`, `xferAsciiString`, `xferUnsignedShort`

### `xfer`
- Purpose: Handles full game client state serialization/deserialization
- Calls: `xferDrawableTOC`, `xferSnapshot`, `findTOCEntryById`, `newDrawable`

## Globals
- `TheGameClient` (GameClient*): Singleton instance of GameClient

## Dependencies
- Key includes: `GameClient.h`, `Common/GameEngine.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`
- External symbols: `TheMessageStream`, `TheThingFactory`, `TheGameLogic`, `TheDrawGroupInfo`
