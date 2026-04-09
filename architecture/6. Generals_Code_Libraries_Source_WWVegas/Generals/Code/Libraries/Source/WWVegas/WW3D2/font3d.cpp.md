# Generals/Code/Libraries/Source/WWVegas/WW3D2/font3d.cpp

## Purpose
Handles 3D font rendering, including loading, processing, and displaying text with proportional or monospace spacing.

## Responsibilities
- Load and process font images (TGA) into textures
- Convert monospace fonts to proportional fonts
- Manage font rendering parameters (spacing, scaling)
- Calculate string dimensions for layout

## Key Types
- **Font3DDataClass**: Manages font texture and UV tables
- **Font3DInstanceClass**: Handles font rendering instances with spacing/scaling
- **SurfaceClass** (external): Used for font image processing
- **TextureClass** (external): Font texture storage

## Key Functions
### `Font3DDataClass::Load_Font_Image`
- Purpose: Loads TGA font image and builds UV tables
- Calls: `SurfaceClass` methods, `Make_Proportional`, `Minimize_Font_Image`

### `Font3DDataClass::Make_Proportional`
- Purpose: Converts monospace font to proportional by tightening character bounds
- Calls: `SurfaceClass::FindBB`, `Minimize_Font_Image`

### `Font3DDataClass::Minimize_Font_Image`
- Purpose: Repacks font into smallest power-of-2 texture
- Calls: `SurfaceClass::Copy`, `SurfaceClass::Clear`

### `Font3DInstanceClass::String_Width`
- Purpose: Calculates string width for layout
- Calls: `Char_Spacing` (internal)

## Globals
- `_surface` (SurfaceClass*): Temporary surface during font processing

## Dependencies
- `font3d.h`, `assetmgr.h`, `texture.h`, `surfaceclass.h`, `vector2i.h`
- Uses `WW3DAssetManager`, `TextureClass`, `SurfaceClass`
