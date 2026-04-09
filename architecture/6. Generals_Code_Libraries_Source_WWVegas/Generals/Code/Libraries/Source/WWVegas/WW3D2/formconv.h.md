# Generals/Code/Libraries/Source/WWVegas/WW3D2/formconv.h

## Purpose
Header file for converting between WW3D and Direct3D texture format enums.

## Responsibilities
- Declares conversion functions between WW3DFormat and D3DFORMAT
- Provides initialization for format conversion
- Exposes format conversion utilities for rendering pipeline

## Key Types
None

## Key Functions
### WW3DFormat_To_D3DFormat
- Purpose: Converts WW3DFormat to D3DFORMAT
- Calls: Not inferable

### D3DFormat_To_WW3DFormat
- Purpose: Converts D3DFORMAT to WW3DFormat
- Calls: Not inferable

### Init_D3D_To_WW3_Conversion
- Purpose: Initializes the conversion between D3D and WW3 formats
- Calls: Not inferable

## Globals
None

## Dependencies
- `ww3dformat.h`: WW3D format definitions
- `<d3d8.h>`: Direct3D 8 format definitions
