# Generals/Code/Libraries/Source/WWVegas/WWLib/hsv.h

## Purpose
Defines the HSVClass for hue-saturation-value color representation and manipulation.

## Responsibilities
- Encapsulate HSV color data (hue, saturation, value)
- Provide conversion to RGB
- Offer color adjustment and difference calculation
- Manage color value ranges (0-255)

## Key Types
- **HSVClass (Class)**: Represents a color in HSV space with hue, saturation, and value components.
- **RGBClass (Class)**: Forward-declared RGB color class (defined elsewhere).
- **(anonymous enum) (Enum)**: Contains MAX_VALUE constant (255).

## Key Functions
### HSVClass::Adjust
- Purpose: Adjusts HSV values based on a ratio and another HSV color.
- Calls: Not inferable.

### HSVClass::Difference
- Purpose: Computes the difference between two HSV colors.
- Calls: Not inferable.

### HSVClass::Get_Hue/Get_Saturation/Get_Value
- Purpose: Getter methods for HSV components.
- Calls: None.

### HSVClass::Set_Hue/Set_Saturation/Set_Value
- Purpose: Setter methods for HSV components.
- Calls: None.

## Globals
- **BlackColor (HSVClass const)**: Static black color instance.

## Dependencies
- Forward declaration of RGBClass.
- No external symbols used.
