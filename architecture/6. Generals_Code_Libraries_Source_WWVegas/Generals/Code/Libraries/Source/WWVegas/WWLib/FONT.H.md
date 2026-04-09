# Generals/Code/Libraries/Source/WWVegas/WWLib/FONT.H

## Purpose
Defines the abstract base class for font rendering in the SAGE engine.

## Responsibilities
- Declares the `FontClass` interface for text measurement and rendering
- Specifies virtual methods for character/pixel width calculation
- Defines text printing with clipping and color remapping
- Provides spacing adjustment methods

## Key Types
- `FontClass` (Class): Abstract base class for font rendering operations

## Key Functions
### `Char_Pixel_Width`
- Purpose: Returns the pixel width of a single character
- Calls: None

### `String_Pixel_Width`
- Purpose: Returns the pixel width of a string
- Calls: None

### `Print`
- Purpose: Renders text to a surface with clipping and optional color remapping
- Calls: None

### `Set_XSpacing` / `Set_YSpacing`
- Purpose: Adjusts horizontal/vertical spacing between characters
- Calls: None

## Globals
- None

## Dependencies
- `convert.h` (ConvertClass)
- `point.h` (Point2D)
- `trect.h` (Rect)
- `Surface` (forward declaration)
