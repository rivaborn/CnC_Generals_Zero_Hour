# GeneralsMD/Code/GameEngine/Include/GameClient/GameFont.h

## Purpose
Defines the `GameFont` and `FontLibrary` classes for managing fonts in the game engine.

## Responsibilities
- Declares the `GameFont` class representing a font resource.
- Declares the `FontLibrary` class for managing a collection of fonts.
- Provides interfaces for font retrieval, iteration, and lifecycle management.

## Key Types
- **GameFont (Class)**: Represents a font with properties like name, point size, height, and bold flag.
- **FontLibrary (Class)**: Manages a collection of fonts and provides access to them.
- **GameFontMagicEnum (Enum)**: Not inferable (placeholder).
- **GameFont_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (placeholder).

## Key Functions
### `FontLibrary::getFont`
- Purpose: Retrieves a font by name, point size, and bold flag.
- Calls: Not inferable (implementation not shown).

### `FontLibrary::firstFont`
- Purpose: Returns the first font in the library.
- Calls: None.

### `FontLibrary::nextFont`
- Purpose: Returns the next font in the library after a given font.
- Calls: None.

### `FontLibrary::loadFontData`
- Purpose: Loads font data for a given font (pure virtual).
- Calls: None.

## Globals
- **TheFontLibrary (FontLibrary*)**: Global instance of the font library.

## Dependencies
- `Common/SubsystemInterface.h`
- `Lib/BaseType.h`
- `Common/AsciiString.h`
- `Common/GameMemory.h`
