# Generals/Code/Tools/GUIEdit/Include/GUIEditColor.h

## Purpose
Defines color structures and a color selection function for the GUI editor.

## Responsibilities
- Declares integer and real-based RGB color structures
- Declares HSV color structure
- Provides a color selection function interface

## Key Types
- RGBColorInt (struct): Integer-based RGBA color representation
- RGBColorReal (struct): Floating-point RGBA color representation (0.0-1.0)
- HSVColorReal (struct): Floating-point HSV color representation with alpha

## Key Functions
### SelectColor
- Purpose: Displays a color picker dialog and returns selected color
- Calls: Not inferable (implementation not shown)

## Globals
- None

## Dependencies
- Uses `Int` and `Real` types (not defined here)
- No external includes visible in header
