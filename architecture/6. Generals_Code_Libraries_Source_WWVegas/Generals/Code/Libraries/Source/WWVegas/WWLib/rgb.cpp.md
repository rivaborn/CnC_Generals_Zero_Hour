# Generals/Code/Libraries/Source/WWVegas/WWLib/rgb.cpp

## Purpose
Implements RGB color manipulation and conversion to HSV color space.

## Responsibilities
- RGB color adjustment toward another color
- Calculating color difference magnitude
- Converting RGB to HSV color space

## Key Types
- RGBClass (Class): Represents a color with red, green, blue components
- HSVClass (Class): HSV color representation (used in conversion operator)

## Key Functions
### RGBClass::Adjust
- Purpose: Adjusts RGB values toward another color based on a ratio
- Calls: None

### RGBClass::Difference
- Purpose: Calculates the relative distance between two colors
- Calls: None

### RGBClass::operator HSVClass
- Purpose: Converts RGB color to HSV color space
- Calls: None

## Globals
- BlackColor (RGBClass const): Predefined black color (0,0,0)

## Dependencies
- always.h, hsv.h, palette.h, rgb.h
- Uses HSVClass from hsv.h
