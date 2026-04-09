# Generals/Code/Tools/Autorun/TTFont.h

## Purpose
Header file defining TrueType font handling classes and types for text rendering in the game.

## Responsibilities
- Declares font-related enums for text formatting, shadows, and special effects
- Defines TTFontClass for font management and rendering
- Provides FontManagerClass for global font access
- Declares global font pointers and color constants

## Key Types
- TextPrintType (Enum): Font size and type flags
- TextShadowType (Enum): Shadow rendering options
- TextFormatType (Enum): Text alignment and formatting flags
- SpecialEffectType (Enum): Special text rendering effects
- TTFontClass (Class): TrueType font management and rendering
- FontManagerClass (Class): Global font manager

## Key Functions
### Font_From_TPF
- Purpose: Returns font pointer based on flags
- Calls: Not inferable

### Is_True_Type_Font
- Purpose: Checks if flags indicate TrueType font
- Calls: Not inferable

## Globals
- BackBufferDC (HDC): Global device context for rendering
- TEXT_COLOR (unsigned long): Default text color
- WHITE_COLOR (unsigned long): White color constant
- FontManager (FontManagerClass*): Global font manager instance
- TTButtonFontPtr (TTFontClass*): Button font pointer
- TTTextFontPtr (TTFontClass*): Main text font pointer

## Dependencies
- stddef.h, point.h, rect.h
- Windows GDI types (HDC, HFONT, COLORREF)
- External font creation/drawing functions
