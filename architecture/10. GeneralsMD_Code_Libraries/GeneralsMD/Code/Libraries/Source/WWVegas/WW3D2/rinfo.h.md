# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rinfo.h

## Purpose
Defines rendering information classes for the WW3D engine, including camera data, material passes, and special rendering modes.

## Responsibilities
- Manages render state via `RenderInfoClass`
- Handles material pass stacking and override flags
- Provides special rendering modes (visibility detection, shadow rendering)
- Maintains camera and lighting environment references

## Key Types
- `RenderInfoClass` (Class): Core rendering state container
- `SpecialRenderInfoClass` (Class): Extended render info for special operations
- `RINFO_OVERRIDE_FLAGS` (Enum): Rendering override flags
- `MaterialPassClass` (Class): Material pass reference (forward declared)
- `LightEnvironmentClass` (Class): Lighting data reference (forward declared)

## Key Functions
### `Push_Material_Pass`
- Purpose: Adds a material pass to the render stack
- Calls: None visible

### `Push_Override_Flags`
- Purpose: Pushes override flags onto the stack
- Calls: None visible

### `SpecialRenderInfoClass(CameraClass &, int)`
- Purpose: Constructs special render info with type-specific setup
- Calls: `RenderInfoClass` constructor

## Globals
- `MAX_ADDITIONAL_MATERIAL_PASSES` (const unsigned): Max additional passes (32)
- `MAX_OVERRIDE_FLAG_LEVEL` (const unsigned): Max override flag depth (32)

## Dependencies
- `CameraClass`, `MaterialPassClass`, `LightEnvironmentClass`, `VisRasterizerClass`, `BWRenderClass`, `TexProjectClass`
- Includes: `always.h`, `bittype.h`, `ww3d.h`, `wwdebug.h`, `shader.h`, `vector.h`, `matrix3
