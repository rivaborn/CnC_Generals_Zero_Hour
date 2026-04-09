# Generals/Code/Libraries/Source/WWVegas/WW3D2/ww3dformat.cpp

## Purpose
Handles texture format conversions and utilities for the WW3D (Westwood 3D) engine.

## Responsibilities
- Convert between color formats (Vector4, unsigned int, WW3DFormat)
- Determine valid texture formats based on hardware capabilities
- Extract luminance from RGB using CIE 709 standard
- Parse TGA headers to determine source texture format

## Key Types
- `WW3DFormat` (Enum): Texture format identifiers (e.g., `WW3D_FORMAT_R8G8B8`, `WW3D_FORMAT_A8R8G8B8`)
- `Vector4` (Struct): 4D vector representing RGBA color
- `Targa` (Struct): TGA file header data

## Key Functions
### `RGB_to_CIEY`
- Purpose: Convert RGB to luminance using CIE 709 standard.
- Calls: None

### `Vector4_to_Color`
- Purpose: Convert Vector4 color to specified WW3DFormat.
- Calls: `RGB_to_CIEY`, `DX8Wrapper::Convert_Color`

### `Color_to_Vector4`
- Purpose: Convert WW3DFormat color to Vector4.
- Calls: `RGB_to_CIEY`

### `Get_WW3D_Format`
- Purpose: Determine texture format from TGA header.
- Calls: `Get_Valid_Texture_Format`

### `Get_Valid_Texture_Format`
- Purpose: Ensure texture format is supported by hardware.
- Calls: `DX8Caps::Support_DXTC`, `DX8Caps::Support_Texture_Format`, `WW3D::Get_Texture_Compression_Mode`, `WW3D::Get_Device_Resolution`

### `Get_Bytes_Per_Pixel`
- Purpose: Return bytes per pixel for a given WW3DFormat.
- Calls: None

## Globals
None

## Dependencies
- `ww3dformat.h`, `vector4.h`, `wwdebug.h`, `targa.h`, `dx8wrapper.h`, `dx8caps.h`, `<d3d8.h>`
- `DX8Wrapper`, `DX8Caps`, `WW3D` (external classes/functions)
