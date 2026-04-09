# Generals/Code/Libraries/Source/WWVegas/WW3D2/texproject.h

## Purpose
Defines the `TexProjectClass` for projecting textures onto 3D objects in the game world, including shadow and dynamic texture projections.

## Responsibilities
- Manages texture projection parameters (size, intensity, attenuation)
- Handles projection types (perspective/ortho) and rendering targets
- Integrates with culling and rendering systems
- Supports dynamic texture updates and material passes

## Key Types
- **TexProjectClass (Class)**: Main texture projection class with projection, culling, and list management.
- **FlagsType (Enum)**: Bit flags for projection options (perspective, additive, attenuation, etc.).
- **TexProjListClass (Class)**: Container for managing multiple texture projectors.
- **TexProjListIterator (Class)**: Iterator for traversing texture projector lists.

## Key Functions
### `Set_Perspective_Projection`
- Purpose: Configures perspective projection parameters.
- Calls: None visible.

### `Set_Ortho_Projection`
- Purpose: Configures orthographic projection parameters.
- Calls: None visible.

### `Compute_Texture`
- Purpose: Generates the projection texture from a render object.
- Calls: Not inferable.

### `Pre_Render_Update`
- Purpose: Updates projection state before rendering.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- Key includes: `matrix3d.h`, `matrix4.h`, `obbox.h`, `matpass.h`, `matrixmapper.h`, `cullsys.h`, `multilist.h`, `projector.h`
- External symbols: `SpecialRenderInfoClass`, `RenderObjClass`, `MaterialPassClass`, `SurfaceClass`, `TextureClass`, `CameraClass`
