# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/formconv.cpp

## Purpose
Converts between Westwood 3D (WW3D) and Direct3D (D3D) texture and depth-stencil format enums.

## Responsibilities
- Maintains conversion lookup tables for WW3D â D3D formats
- Provides conversion functions for texture formats
- Provides conversion functions for depth-stencil formats
- Initializes reverse conversion tables at runtime

## Key Types
- `WW3DFormat` (Enum): WW3D texture format enum
- `WW3DZFormat` (Enum): WW3D depth-stencil format enum
- `D3DFORMAT` (External): Direct3D texture format enum

## Key Functions
### `WW3DFormat_To_D3DFormat`
- Purpose: Converts WW3D texture format to D3D format
- Calls: None

### `D3DFormat_To_WW3DFormat`
- Purpose: Converts D3D texture format to WW3D format
- Calls: None

### `WW3DZFormat_To_D3DFormat`
- Purpose: Converts WW3D depth-stencil format to D3D format
- Calls: None

### `D3DFormat_To_WW3DZFormat`
- Purpose: Converts D3D depth-stencil format to WW3D format
- Calls: None

### `Init_D3D_To_WW3_Conversion`
- Purpose: Initializes reverse conversion tables
- Calls: None

## Globals
- `WW3DFormatToD3DFormatConversionArray` (D3DFORMAT[]): Forward texture format lookup
- `WW3DZFormatToD3DFormatConversionArray` (D3DFORMAT[]): Forward depth-stencil format lookup
- `D3DFormatToWW3DFormatConversionArray` (WW3DFormat[]): Reverse texture format lookup
- `D3DFormatToWW3DZFormatConversionArray` (WW3DZFormat[]): Reverse depth-stencil format lookup

## Dependencies
- `formconv.h` (header)
- `D3DFORMAT` (Direct3D enum)
- `_XBOX` (platform macro)
