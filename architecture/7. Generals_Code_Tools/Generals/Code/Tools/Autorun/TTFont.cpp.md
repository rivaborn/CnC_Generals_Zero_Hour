# Generals/Code/Tools/Autorun/TTFont.cpp

## Purpose
Handles TrueType font rendering and management for the game's setup/autorun tool.

## Responsibilities
- Manages font creation and destruction
- Provides text measurement and rendering utilities
- Supports multiple languages (Japanese, Korean, Chinese, English, French, German)
- Maintains global font pointers and color definitions

## Key Types
- `TTFontClass`: TrueType font wrapper with rendering capabilities
- `FontManagerClass`: Manages multiple font instances
- `TextPrintType` (enum): Font type flags (e.g., TPF_BUTTON_FONT, TPF_TEXT_FONT)

## Key Functions
### `TTFontClass::TTFontClass`
- Purpose: Constructor for TrueType font objects
- Calls: `AddFontResource`, `CreateFont`, `GetTextFace`, `GetTextMetrics`

### `Font_From_TPF`
- Purpose: Maps font flags to font pointers
- Calls: None

### `Is_True_Type_Font`
- Purpose: Checks if flags represent a TrueType font
- Calls: None

## Globals
- `TTButtonFontPtr` (TTFontClass*): Main button font
- `TTTextFontPtr` (TTFontClass*): Main text font
- `FontManager` (FontManagerClass*): Font manager instance
- `TEXT_COLOR` (unsigned long): Default text color
- `BLACK_COLOR`/`WHITE_COLOR`/`RED_COLOR` etc. (unsigned long): Predefined colors

## Dependencies
- Windows GDI functions (`CreateFont`, `GetTextMetrics`, etc.)
- `args.h`, `autorun.h`, `ttfont.h`, `jsupport.h`, `locale_api.h`
- External symbols: `Args`, `LanguageID`, `CodePage`
