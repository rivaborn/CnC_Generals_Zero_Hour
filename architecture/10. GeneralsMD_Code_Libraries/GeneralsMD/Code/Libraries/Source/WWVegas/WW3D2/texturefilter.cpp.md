# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texturefilter.cpp

## Purpose
Manages texture filtering settings for the Direct3D rendering pipeline, including min/mag/mip filters and address modes.

## Responsibilities
- Initializes texture filter modes based on hardware capabilities
- Applies texture filter states to Direct3D texture stages
- Handles anisotropic, trilinear, and basic filtering modes
- Manages texture address wrapping/clamping
- Provides filter configuration abstraction

## Key Types
- **TextureFilterClass (Class)**: Main texture filter configuration class
- **FilterType (Enum)**: Filter quality levels (NONE, FAST, BEST, DEFAULT)
- **MipCountType (Enum)**: Mip level count options
- **TextureFilterMode (Enum)**: Filter mode presets (NORMAL, TRILINEAR, ANISOTROPIC)

## Key Functions
### `Apply(unsigned int stage)`
- Purpose: Applies current filter settings to a specific texture stage
- Calls: `DX8Wrapper::Set_DX8_Texture_Stage_State`

### `_Init_Filters(TextureFilterMode filter_type)`
- Purpose: Initializes filter lookup tables based on hardware capabilities
- Calls: `DX8Wrapper::Get_Current_Caps()->Get_DX8_Caps()`

### `Set_Mip_Mapping(FilterType mipmap)`
- Purpose: Configures mipmapping filter type
- Calls: None

### `_Set_Default_Min_Filter(FilterType filter)`
- Purpose: Sets default minification filter for all stages
- Calls: None

### `_Set_Default_Mag_Filter(FilterType filter)`
- Purpose: Sets default magnification filter for all stages
- Calls: None

### `_Set_Default_Mip_Filter(FilterType filter)`
- Purpose: Sets default mipmapping filter for all stages
- Calls: None

## Globals
- `_MinTextureFilters (unsigned[MAX_TEXTURE_STAGES][FILTER_TYPE_COUNT])`: Minification filter lookup table
- `_MagTextureFilters (unsigned[MAX_TEXTURE_STAGES][FILTER_TYPE_COUNT])`: Magnification filter lookup table
- `_MipMapFilters (unsigned[MAX_TEXTURE_STAGES][FILTER_TYPE_COUNT])`: Mipmapping filter lookup table

## Dependencies
- `texturefilter.h`: Header with class declarations
- `dx8wrapper.h`: Direct3D wrapper interface
- Direct3D 8 constants (D3DTEXF_*, D3DTSS_*, D3DTADDRESS_*)
