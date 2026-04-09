# Generals/Code/Libraries/Source/WWVegas/WW3D2/ww3dformat.h

## Purpose
Defines pixel format enums and utility functions for texture handling in the WW3D rendering system.

## Responsibilities
- Declares `WW3DFormat` enum for supported texture formats
- Provides format utility functions (alpha checks, bit counts, conversions)
- Defines texture format conversion and validation routines

## Key Types
- `WW3DFormat` (Enum): pixel format identifiers (e.g., `WW3D_FORMAT_R8G8B8`, `WW3D_FORMAT_DXT1`)
- `Vector4` (Class): color/vertex data structure (external)
- `Targa` (Class): TGA image data structure (external)

## Key Functions
### `Has_Alpha(WW3DFormat format)`
- Purpose: Checks if a format includes an alpha channel.
- Calls: None

### `Alpha_Bits(WW3DFormat format)`
- Purpose: Returns the number of alpha bits in a format.
- Calls: None

### `Vector4_to_Color(unsigned int *outc, const Vector4 &inc, WW3DFormat format)`
- Purpose: Converts a `Vector4` color to a packed integer in the specified format.
- Calls: None

### `Color_to_Vector4(Vector4* outc, const unsigned int inc, WW3DFormat format)`
- Purpose: Converts a packed integer color to a `Vector4` in the specified format.
- Calls: None

### `Get_WW3D_Format(WW3DFormat& dest_format, WW3DFormat& src_format, unsigned& src_bpp, const Targa& targa)`
- Purpose: Determines appropriate WW3D format from a TGA header.
- Calls: None

### `Get_Valid_
