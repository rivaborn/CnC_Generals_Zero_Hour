# Generals/Code/Libraries/Source/WWVegas/WW3D2/formconv.cpp

## Purpose
Converts between WW3D and Direct3D texture format enums.

## Responsibilities
- Maps WW3D formats to D3D formats
- Maps D3D formats to WW3D formats
- Initializes conversion lookup tables

## Key Types
- `WW3DFormat` (Enum): WW3D texture format enum
- `D3DFORMAT` (Enum): Direct3D texture format enum

## Key Functions
### `WW3DFormat_To_D3DFormat`
- Purpose: Converts WW3D format to D3D format
- Calls: None

### `D3DFormat_To_WW3DFormat`
- Purpose: Converts D3D format to WW3D format
- Calls: None

### `Init_D3D_To_WW3_Conversion`
- Purpose: Initializes D3D-to-WW3D conversion table
- Calls: None

## Globals
- `WW3DFormatToD3DFormatConversionArray` (D3DFORMAT[]): Maps WW3D formats to D3D formats
- `D3DFormatToWW3DFormatConversionArray` (WW3DFormat[]): Maps D3D formats to WW3D formats

## Dependencies
- `formconv.h` (header)
- `D3DFORMAT` (Direct3D enum)
- `WW3DFormat` (WW3D enum)
