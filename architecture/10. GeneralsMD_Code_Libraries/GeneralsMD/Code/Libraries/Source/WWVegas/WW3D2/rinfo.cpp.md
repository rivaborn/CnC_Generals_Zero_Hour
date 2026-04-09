# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rinfo.cpp

## Purpose
Implements render state management classes for the WW3D2 rendering engine.

## Responsibilities
- Manages render info state (fog, lights, material passes)
- Handles override flags for rendering
- Provides special render info for different render types
- Tracks additional material passes and rejected passes

## Key Types
- **RenderInfoClass (Class)**: Main render state container (fog, lights, material passes)
- **SpecialRenderInfoClass (Class)**: Extended render info for special render types
- **RINFO_OVERRIDE_FLAGS (Enum)**: Render override flags (not shown in snippet)

## Key Functions
### `Push_Material_Pass`
- Purpose: Adds a material pass to the render info
- Calls: `Add_Ref()` on the material pass

### `Pop_Material_Pass`
- Purpose: Removes the last material pass from the render info
- Calls: `Release_Ref()` on the material pass

### `Push_Override_Flags`
- Purpose: Pushes override flags onto the stack
- Calls: None

### `Pop_Override_Flags`
- Purpose: Pops override flags from the stack
- Calls: None

## Globals
- None

## Dependencies
- `rinfo.h`, `camera.h`, `matpass.h`
- `CameraClass`, `MaterialPassClass` (external)
- `WWASSERT` macro (assertion)
