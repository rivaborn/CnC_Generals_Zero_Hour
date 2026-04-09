# GeneralsMD/Code/GameEngine/Include/GameClient/GameClient.h

## Purpose
Defines the GameClient singleton class, the core interface for game operations including drawables, UI, and rendering.

## Responsibilities
- Manages drawable objects and their lifecycle
- Handles game frame updates and time-of-day settings
- Provides region-based drawable iteration
- Manages game message translation and dispatching
- Maintains drawable lookup tables and TOC (Table of Contents)

## Key Types
- **GameClient (Class)**: Core singleton managing game client operations
- **GameClientMessageDispatcher (Class)**: Handles client-side message translation
- **DrawableTOCEntry (Struct)**: Stores name-ID pairs for drawable TOC
- **DrawableTOCList (Class)**: List of DrawableTOCEntry objects
- **TextBearingDrawableList (Class)**: List of drawables with text bearings
- **(anonymous enum)**: Contains MAX_CLIENT_TRANSLATORS constant

## Key Functions
### `registerDrawable`
- Purpose: Registers a drawable with the GameClient and assigns it a unique ID
- Calls: `allocDrawableID`, `addDrawableToLookupTable`

### `iterateDrawablesInRegion`
- Purpose: Iterates over drawables within a specified region
- Calls: `userFunc` (callback)

### `findDrawableByID`
- Purpose: Retrieves a drawable by its ID
- Calls: None (direct lookup)

### `addTOCEntry`
- Purpose: Adds a name-ID pair to the drawable TOC
- Calls: None

## Globals
- **TheGameClient (GameClient*)**: The singleton GameClient instance

## Dependencies
- `common/GameType.h`, `Common/MessageStream.h`, `Common/Snapshot.h`, `Common/STLTypedefs.h`, `Common/SubsystemInterface.h`, `GameClient/CommandXlat.h`, `GameClient/Drawable.h`
- Forward declarations for multiple game subsystem classes (Display, FontLibrary, etc.)
