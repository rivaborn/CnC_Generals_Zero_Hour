# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/colorspace.h

## Purpose
Provides color space conversion utilities between RGB and HSV color models.

## Responsibilities
- Convert RGB to HSV color space
- Convert HSV to RGB color space
- Apply color recoloring using HSV shifts
- Handle color conversions for both Vector3 and unsigned RGBA formats

## Key Types
- None

## Key Functions
### RGB_To_HSV
- Purpose: Convert RGB color to HSV color space
- Calls: WWMath::Max, WWMath::Min

### HSV_To_RGB
- Purpose: Convert HSV color to RGB color space
- Calls: WWMath::Floor

### Recolor (Vector3)
- Purpose: Apply HSV shift to RGB color
- Calls: RGB_To_HSV, HSV_To_RGB, WWMath::Clamp

### Recolor (unsigned)
- Purpose: Apply HSV shift to RGBA color
- Calls: DX8Wrapper::Convert_Color, Recolor (Vector3)

## Globals
- None

## Dependencies
- dx8wrapper.h
- wwmath.h
- Vector3, Vector4 classes
- DX8Wrapper::Convert_Color function
