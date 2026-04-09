# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texproject.h

## Purpose
Defines the `TexProjectClass` for projecting textures onto 3D objects in the game world, including shadows and dynamic projections.

## Responsibilities
- Manages texture projection parameters (size, intensity, attenuation)
- Handles projection types (perspective/ortho) and rendering targets
- Integrates with culling and rendering systems
- Supports dynamic and static object projections

## Key Types
- **TexProjectClass (Class)**: Main texture projection class with projection logic
- **FlagsType (Enum)**: Bitflags for projection options (perspective, additive, attenuation, etc.)
- **TexProjListClass (Class)**: Container for managing multiple texture projectors

## Key Functions
### TexProjectClass()
- Purpose: Constructor for texture projector
- Calls: Not inferable

### Set_Texture_Size(int size)
- Purpose: Sets the texture size for projection
- Calls: Not inferable

### Compute_Perspective_Projection(RenderObjClass * obj, ...)
- Purpose: Computes perspective projection for a render object
- Calls: Not inferable

### Pre_Render_Update(const Matrix3D & camera)
- Purpose: Updates projection before rendering
- Calls: Not inferable

## Globals
- None

## Dependencies
- `matrix3d.h`, `matrix4.h`, `obbox.h`, `matpass.h`, `matrixmapper.h`, `cullsys.h`, `multilist.h`, `projector.h`
- `SpecialRenderInfoClass`, `RenderObjClass`, `MaterialPassClass`, `SurfaceClass`, `TextureClass`, `ZTextureClass`
