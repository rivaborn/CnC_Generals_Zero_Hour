# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ddsfile.h

## Purpose
Header file defining structures and classes for loading and manipulating DirectDraw Surface (DDS) files, including support for textures, cube maps, and volume textures.

## Responsibilities
- Define legacy DirectX 7 structures for DDS file compatibility
- Provide a class for loading and accessing DDS file data
- Support texture formats, mipmapping, and color conversion
- Handle cube maps and volume textures
- Offer methods for copying texture data to surfaces

## Key Types
- **LegacyDDCOLORKEY (struct)**: Represents old DX7 color key structure
- **LegacyDDSCAPS2 (struct)**: Represents old DX7 surface capabilities
- **LegacyDDPIXELFORMAT (struct)**: Represents old DX7 pixel format
- **LegacyDDSURFACEDESC2 (struct)**: Old DX7 surface description structure
- **DDSType (enum)**: Type of DDS file (texture, cubemap, volume)
- **DDSFileClass (class)**: Main class for loading and manipulating DDS files

## Key Functions
### DDSFileClass::Load
- Purpose: Load DDS file data into memory
- Calls: Not inferable (implementation in .cpp)

### DDSFileClass::Copy_Level_To_Surface
- Purpose: Copy texture level data to a Direct3D surface
- Calls: Not inferable

### DDSFileClass::Get_4x4_Block
- Purpose: Decompress a 4x4 block from compressed texture data
- Calls: Not inferable

## Globals
- **Calculate_DXTC_Surface_Size (static function)**: Calculates surface size for DXT compression formats

## Dependencies
- "always.h", "ww3dformat.h", "wwstring.h", "vector3.h"
- IDirect3DSurface8, IDirect3DVolume8 (forward declarations)
- WW3DFormat enum (from ww3dformat.h)
