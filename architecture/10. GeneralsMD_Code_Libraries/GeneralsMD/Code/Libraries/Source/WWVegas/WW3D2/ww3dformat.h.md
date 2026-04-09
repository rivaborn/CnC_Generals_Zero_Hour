# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3dformat.h

## Purpose
Defines texture and depth-stencil format enums and utility functions for the WW3D rendering engine.

## Responsibilities
- Declares format enums (WW3DFormat, WW3DZFormat)
- Provides format utility functions (alpha checks, bit counts, conversions)
- Defines texture format validation and naming functions

## Key Types
- Vector4 (Class): 4D vector type
- Targa (Class): Targa image format handler
- WW3DFormat (Enum): Texture pixel formats (e.g., RGBA8888, DXT1)
- WW3DZFormat (Enum): Depth-stencil buffer formats (e.g., D24S8)

## Key Functions
### Has_Alpha
- Purpose: Checks if a format has alpha channel
- Calls: None

### Alpha_Bits
- Purpose: Returns number of alpha bits in a format
- Calls: None

### Vector4_to_Color
- Purpose: Converts Vector4 to color in specified format
- Calls: None

### Color_to_Vector4
- Purpose: Converts color to Vector4
- Calls: None

### Get_WW3D_Format
- Purpose: Determines format from Targa header
- Calls: None

### Get_Valid_Texture_Format
- Purpose: Finds hardware-compatible texture format
- Calls: None

### Get_Bytes_Per_Pixel
- Purpose: Returns bytes per pixel for a format
- Calls: None

### Get_WW3D_Format_Name
- Purpose: Gets string name for a format
- Calls: None

### Get_Num_Depth_Bits
- Purpose: Returns depth bits for a Z-format
- Calls: None

### Get_Num_Stencil_Bits
- Purpose: Returns stencil bits for a Z-format
- Calls: None

## Globals
None

## Dependencies
- "always.h"
- "wwstring.h"
- Vector4, Targa (forward declarations)
- StringClass (used in Get_WW3D_Format_Name)
