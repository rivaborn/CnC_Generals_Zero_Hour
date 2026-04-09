# Generals/Code/Tools/WW3D/pluglib/rgb.cpp

## Purpose
Implements RGB color manipulation functions including color adjustment, difference calculation, and RGB-to-HSV conversion.

## Responsibilities
- Color adjustment with ratio-based interpolation
- Color difference calculation for palette remapping
- RGB to HSV color space conversion

## Key Types
- **RGBClass**: Represents an RGB color with red, green, blue components
- **HSVClass**: HSV color representation (used in conversion operator)

## Key Functions
### RGBClass::Adjust
- Purpose: Adjusts RGB values toward a target color based on a ratio
- Calls: None

### RGBClass::Difference
- Purpose: Calculates the relative distance between two colors
- Calls: None

### RGBClass::operator HSVClass
- Purpose: Converts RGB color to HSV color space
- Calls: None

## Globals
- **BlackColor (RGBClass)**: Predefined black color constant

## Dependencies
- Key includes: "always.h", "hsv.h", "palette.h", "rgb.h"
- External symbols: HSVClass (defined elsewhere)
