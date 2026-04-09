# GeneralsMD/Code/GameEngine/Include/GameClient/DisplayString.h

## Purpose
Defines the `DisplayString` class for managing and rendering Unicode text in the game.

## Responsibilities
- Store Unicode text and associated display properties (font, clipping region).
- Provide methods for text manipulation (setting, appending, removing characters).
- Support text rendering with optional drop shadows and word wrapping.
- Manage linked list of display strings via `next`/`prev` pointers.

## Key Types
- **DisplayString (Class)**: Base class for text rendering with Unicode support.
- **DisplayStringManager (Class)**: Friend class managing `DisplayString` instances.
- **DisplayStringMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **DisplayString_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### `setText`
- Purpose: Sets the Unicode text content.
- Calls: None (direct).

### `draw`
- Purpose: Renders text at specified coordinates with color/drop shadow.
- Calls: None (pure virtual).

### `getSize`
- Purpose: Retrieves rendered text dimensions.
- Calls: None (pure virtual).

### `appendChar`
- Purpose: Appends a Unicode character to the text.
- Calls: None (direct).

## Globals
- None.

## Dependencies
- `GameFont.h`, `Color.h`, `UnicodeString.h`, `MemoryPoolObject`.
- Forward declaration: `DisplayStringManager`.
