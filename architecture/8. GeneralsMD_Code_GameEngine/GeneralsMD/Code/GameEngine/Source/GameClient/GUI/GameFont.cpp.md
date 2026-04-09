# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameFont.cpp

## Purpose
Manages font resources and provides access to fonts in the game.

## Responsibilities
- Maintains a linked list of loaded fonts
- Loads and unloads font data as needed
- Provides font retrieval by name, size, and style
- Handles font library initialization and cleanup

## Key Types
- **FontLibrary (Class)**: Manages the collection of fonts and their loading/unloading
- **GameFont (Class)**: Represents an individual font resource (defined elsewhere)

## Key Functions
### `FontLibrary::linkFont`
- Purpose: Adds a font to the library's linked list
- Calls: None

### `FontLibrary::unlinkFont`
- Purpose: Removes a font from the library's linked list
- Calls: `DEBUG_CRASH`

### `FontLibrary::deleteAllFonts`
- Purpose: Cleans up all loaded fonts in the library
- Calls: `unlinkFont`, `releaseFontData`

### `FontLibrary::getFont`
- Purpose: Retrieves a font by name, size, and style, loading it if necessary
- Calls: `newInstance`, `loadFontData`, `linkFont`, `DEBUG_CRASH`

## Globals
- **TheFontLibrary (FontLibrary*)**: Global pointer to the font library instance

## Dependencies
- `GameClient/GameFont.h` (header)
- `PreRTS.h` (engine precompiled header)
- `DEBUG_CRASH`, `newInstance`, `loadFontData`, `releaseFontData` (external functions)
- `AsciiString`, `Bool`, `Int` (basic types)
