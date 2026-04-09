# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/font3d.cpp

## Purpose
Handles 3D font rendering by managing font textures, character spacing, and surface optimization.

## Responsibilities
- Load and process font images (TGA) into textures
- Convert monospace fonts to proportional fonts
- Optimize font textures via packing and power-of-two sizing
- Provide string width measurement for layout

## Key Types
- **Font3DDataClass**: Manages font texture data and UV tables
- **Font3DInstanceClass**: Handles font rendering instances with scaling/spacing
- **SurfaceClass** (external): Used for font image processing
- **TextureClass** (external): Font texture storage

## Key Functions
### `Minimize_Font_Image`
- Purpose: Repacks font characters into a smaller power-of-two texture
- Calls: `SurfaceClass::Get_Description`, `SurfaceClass::Clear`, `SurfaceClass::Copy`

### `Make_Proportional`
- Purpose: Adjusts character bounding boxes to create proportional spacing
- Calls: `SurfaceClass::Get_Description`, `SurfaceClass::FindBB`

### `Load_Font_Image`
- Purpose: Loads font from TGA and initializes UV tables
- Calls: `NEW_REF(SurfaceClass)`, `SurfaceClass::Is_Transparent_Column`

### `Build_Cached_Tables`
- Purpose: Precomputes scaled character widths/spacing for rendering
- Calls: `FontData->Char_Width`

## Globals
- `_surface` (SurfaceClass*): Temporary surface during font processing

## Dependencies
- `font3d.h`, `assetmgr.h`, `texture.h`, `surfaceclass.h`, `vector2i.h`
- `WW3DAssetManager`, `TextureClass`, `SurfaceClass`
