# GeneralsMD/Code/GameEngine/Source/GameClient/GameClient.cpp

## Purpose
Implements the GameClient singleton, managing client-side game state, rendering, and user interface.

## Responsibilities
- Manages drawable objects and their serialization
- Handles client-side game initialization and cleanup
- Coordinates input, UI, and rendering systems
- Maintains game client state and frame management
- Provides translation and message dispatching

## Key Types
- `GameClient` (Class): Main client singleton managing game state
- `DrawableTOCEntry` (Struct): Table of contents entry for drawable objects
- `shouldSaveDrawable` (Function): Determines if a drawable should be saved

## Key Functions
### `shouldSaveDrawable`
- Purpose: Checks if a drawable should be saved based on its status and object attachment
- Calls: `testDrawableStatus`, `getObject`

### `xferDrawableTOC`
- Purpose: Serializes/deserializes the drawable table of contents
- Calls: `findTOCEntryByName`, `addTOCEntry`, `xferAsciiString`, `xferUnsignedShort`

### `xfer`
- Purpose: Handles serialization/deserialization of the GameClient state
- Calls: `xferDrawableTOC`, `xferSnapshot`, `findTOCEntryById`, `newDrawable`, `destroyDrawable`

## Globals
- `TheGameClient` (GameClient*): The singleton instance of GameClient

## Dependencies
- Key includes: `GameClient/GameClient.h`, `Common/GameEngine.h`, `Common/GameState.h`, `Common/ThingFactory.h`, `GameClient/Drawable.h`
- External symbols: `TheMessageStream`, `TheThingFactory`, `TheGameLogic`, `TheDrawGroupInfo`
