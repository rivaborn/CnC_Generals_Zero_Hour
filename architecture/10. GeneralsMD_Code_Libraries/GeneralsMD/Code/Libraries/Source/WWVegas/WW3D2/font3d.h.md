# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/font3d.h

## Purpose
Defines classes for 3D font rendering in the SAGE engine, handling font texture management and character metrics.

## Responsibilities
- Manage font texture data and character UV coordinates
- Support both monospaced and proportional font rendering
- Provide scaled character dimensions for rendering
- Handle font image loading and optimization

## Key Types
- **Font3DDataClass (Class)**: Font texture data and character metrics
- **Font3DInstanceClass (Class)**: Font instance with scaling and spacing control
- **TextureClass (Class)**: Reference to font texture (external)
- **SurfaceClass (Class)**: Reference to font surface (external)

## Key Functions
### Font3DDataClass::Load_Font_Image
- Purpose: Load font from TGA file
- Calls: Not inferable

### Font3DDataClass::Make_Proportional
- Purpose: Convert monospaced font to proportional
- Calls: Not inferable

### Font3DDataClass::Minimize_Font_Image
- Purpose: Optimize font texture size
- Calls: Not inferable

### Font3DInstanceClass::Build_Cached_Tables
- Purpose: Rebuild scaled character metrics
- Calls: Not inferable

### Font3DInstanceClass::String_Width
- Purpose: Calculate string width in pixels
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `refcount.h`, `vector4.h`, `widestring.h`, `rect.h`
- `TextureClass`, `SurfaceClass` (forward declarations)
