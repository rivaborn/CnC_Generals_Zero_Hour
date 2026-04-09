# Generals/Code/Libraries/Source/WWVegas/WW3D2/ddsfile.h

## Purpose
Header file defining structures and class for loading and manipulating DDS (DirectDraw Surface) texture files, including legacy DirectX 7 compatibility structures.

## Responsibilities
- Define legacy DirectX 7 texture-related structures (color key, caps, pixel format, surface description)
- Provide DDSFileClass for loading and accessing DDS file data
- Support texture format conversion and mipmapping
- Offer pixel/block access methods for texture data

## Key Types
- LegacyDDCOLORKEY (struct): Legacy DirectX 7 color key structure
- LegacyDDSCAPS2 (struct): Legacy DirectX 7 surface capabilities structure
- LegacyDDPIXELFORMAT (struct): Legacy DirectX 7 pixel format structure
- LegacyDDSURFACEDESC2 (struct): Legacy DirectX 7 surface description structure
- DDSFileClass (class): Main class for DDS file loading and manipulation

## Key Functions
### DDSFileClass::Calculate_DXTC_Surface_Size
- Purpose: Calculate size of DXT-compressed surface
- Calls: None

### DDSFileClass::Copy_Level_To_Surface
- Purpose: Copy texture level data to Direct3D surface
- Calls: None (implementation in .cpp)

### DDSFileClass::Get_4x4_Block
- Purpose: Decompress and retrieve a 4x4 block from compressed texture
- Calls: None (implementation in .cpp)

### DDSFileClass::Load
- Purpose: Load DDS file data into memory
- Calls: None (implementation in .cpp)

## Globals
- None

## Dependencies
- "always.h", "ww3dformat.h", "wwstring.h"
- IDirect3DSurface8 (from Direct3D)
- WW3DFormat enum (from ww3dformat.h)
- StringClass (from wwstring.h)
