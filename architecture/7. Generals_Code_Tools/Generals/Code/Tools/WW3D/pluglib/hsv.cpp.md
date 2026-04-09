# Generals/Code/Tools/WW3D/pluglib/hsv.cpp

## Purpose
Implements HSV (Hue, Saturation, Value) color manipulation and conversion to RGB.

## Responsibilities
- Adjust HSV colors toward target colors with a ratio
- Calculate color differences between HSV objects
- Convert HSV colors to RGB colors

## Key Types
- HSVClass: HSV color representation and operations
- RGBClass: RGB color representation (external)

## Key Functions
### HSVClass::Adjust
- Purpose: Adjusts HSV color toward another HSV color by a ratio
- Calls: Get_Value, Get_Saturation, Get_Hue

### HSVClass::Difference
- Purpose: Computes difference between two HSV colors
- Calls: None

### HSVClass::operator RGBClass
- Purpose: Converts HSV color to RGB color
- Calls: Get_Hue, Get_Saturation, Get_Value

## Globals
- HSVClass::BlackColor (HSVClass): Predefined black HSV color

## Dependencies
- "always.h", "hsv.h", "rgb.h"
- RGBClass (external)
