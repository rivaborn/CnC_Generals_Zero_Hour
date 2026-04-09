# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/formconv.h

## Purpose
Header file for format conversion utilities between WW3D and Direct3D formats.

## Responsibilities
- Declares conversion functions between WW3D and D3D formats
- Provides Z-format conversion utilities
- Initializes conversion tables

## Key Types
None

## Key Functions
### WW3DFormat_To_D3DFormat
- Purpose: Converts WW3D format to D3D format
- Calls: Not inferable

### D3DFormat_To_WW3DFormat
- Purpose: Converts D3D format to WW3D format
- Calls: Not inferable

### WW3DZFormat_To_D3DFormat
- Purpose: Converts WW3D Z-format to D3D format
- Calls: Not inferable

### D3DFormat_To_WW3DZFormat
- Purpose: Converts D3D format to WW3D Z-format
- Calls: Not inferable

### Init_D3D_To_WW3_Conversion
- Purpose: Initializes conversion tables between D3D and WW3D formats
- Calls: Not inferable

## Globals
None

## Dependencies
- `ww3dformat.h`: WW3D format definitions
- `<d3d8.h>`: Direct3D 8 format definitions
