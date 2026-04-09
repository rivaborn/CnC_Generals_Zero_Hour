# Generals/Code/Libraries/Source/WWVegas/WW3D2/rinfo.h

## Purpose
Defines rendering information classes for the WW3D engine, including camera data, material passes, and special rendering modes.

## Responsibilities
- Manages rendering state via `RenderInfoClass`
- Handles material pass overrides and additional passes
- Supports special rendering modes (visibility detection, shadows)
- Provides camera access for scene rendering

## Key Types
- **RenderInfoClass (Class)**: Main rendering state container with camera and material pass management.
- **SpecialRenderInfoClass (Class)**: Extends `RenderInfoClass` for special rendering modes (visibility/shadow).
- **RINFO_OVERRIDE_FLAGS (Enum)**: Flags for rendering overrides (two-sided, sorting, additional passes only).
- **RENDER_VIS/RENDER_SHADOW (Enum)**: Special render type identifiers.

## Key Functions
### `Push_Material_Pass`
- Purpose: Adds a material pass to the rendering stack.
- Calls: None visible.

### `Push_Override_Flags`
- Purpose: Pushes override flags onto the stack.
- Calls: None visible.

### `SpecialRenderInfoClass(CameraClass &, int)`
- Purpose: Constructs special render info with a render type.
- Calls: `RenderInfoClass` constructor.

## Globals
- **MAX_ADDITIONAL_MATERIAL_PASSES (const unsigned)**: Max additional material passes (32).
- **MAX_OVERRIDE_FLAG_LEVEL (const unsigned)**: Max override flag stack depth (32).

## Dependencies
- `CameraClass`, `MaterialPassClass`, `LightEnvironmentClass`, `VisRasterizerClass`, `BWRenderClass`
- Includes: `always.h`, `bittype.h`, `ww3d.h`, `wwdebug.h`, `shader.h`, `vector.h`, `matrix3
