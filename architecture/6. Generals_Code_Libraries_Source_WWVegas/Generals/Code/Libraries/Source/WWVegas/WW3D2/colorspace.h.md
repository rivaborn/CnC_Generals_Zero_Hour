# Generals/Code/Libraries/Source/WWVegas/WW3D2/colorspace.h

## Purpose
Provides color space conversion utilities between RGB and HSV color models.

## Responsibilities
- Convert RGB to HSV color space
- Convert HSV to RGB color space
- Apply color recoloring using HSV shifts

## Key Types
None

## Key Functions
### RGB_To_HSV
- Purpose: Convert RGB color to HSV color space
- Calls: WWMath::Max, WWMath::Min

### HSV_To_RGB
- Purpose: Convert HSV color to RGB color space
- Calls: WWMath::Floor

### Recolor
- Purpose: Apply color recoloring using HSV shift values
- Calls: RGB_To_HSV, HSV_To_RGB, WWMath::Clamp

## Globals
None

## Dependencies
- wwmath.h (Vector3, WWMath class)
- Uses Vector3 for color representation
