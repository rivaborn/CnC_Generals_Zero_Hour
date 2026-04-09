# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rgb.cpp

## Purpose
Implements RGB color manipulation utilities, including color adjustment, difference calculation, and RGB-to-HSV conversion.

## Responsibilities
- Provides RGB color class with adjustment and difference operations
- Implements RGB-to-HSV color space conversion
- Defines a global black color constant

## Key Types
- RGBClass (Class): Represents an RGB color with manipulation methods
- HSVClass (Class): HSV color representation (defined elsewhere)
- BlackColor (RGBClass): Global constant for black color

## Key Functions
### RGBClass::Adjust
- Purpose: Adjusts RGB values toward a target color based on a ratio
- Calls: None

### RGBClass::Difference
- Purpose: Calculates the perceptual difference between two colors
- Calls: None

### RGBClass::operator HSVClass
- Purpose: Converts RGB color to HSV color space
- Calls: HSVClass constructor

## Globals
- BlackColor (RGBClass const): Predefined black color (0,0,0)

## Dependencies
- "always.h", "hsv.h", "palette.h", "rgb.h"
- HSVClass (external)
- PaletteClass (external)
