# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3dformat.cpp

## Purpose
Handles texture format conversions and utility functions for WW3D (Westwood 3D) rendering pipeline.

## Responsibilities
- Converts between WW3D format enums and human-readable names
- Translates between Vector4 colors and WW3D format-specific color values
- Determines valid texture formats based on hardware capabilities
- Provides format metadata (bytes per pixel, depth/stencil bits)

## Key Types
- `WW3DFormat` (Enum): Texture format identifiers (R8G8B8, A8R8G8B8, etc.)
- `WW3DZFormat` (Enum): Depth/stencil format identifiers
- `Vector4` (Struct): RGBA color representation

## Key Functions
### Get_WW3D_Format_Name
- Purpose: Returns string name for a WW3DFormat enum value
- Calls: None

### Vector4_to_Color
- Purpose: Converts Vector4 color to format-specific integer color
- Calls: `DX8Wrapper::Convert_Color`, `RGB_to_CIEY`

### Color_to_Vector4
- Purpose: Converts format-specific color to Vector4
- Calls: `RGB_to_CIEY`

### Get_Valid_Texture_Format
- Purpose: Determines hardware-compatible texture format
- Calls: `DX8Wrapper::Get_Current_Caps()->Support_DXTC`, `DX8Wrapper::Get_Current_Caps()->Support_Texture_Format`, `WW3D::Get_Device_Resolution`, `WW3D::Get_Texture_Bitdepth`

### Get_Bytes_Per_Pixel
- Purpose: Returns bytes per pixel for a given format
- Calls: None

### Get_Num_Depth_Bits / Get_Num_Stencil_Bits
- Purpose: Returns bit counts for depth/stencil formats
- Calls: None

## Globals
None

## Dependencies
- `ww3dformat.h`, `vector4.h`, `wwdebug.h`, `targa.h`, `dx8wrapper.h`, `dx8caps.h`, `<d3d8.h>`
- `DX8Wrapper`, `WW3D` classes
- `StringClass`, `Targa` types
