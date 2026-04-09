# Generals/Code/Libraries/Source/WWVegas/WW3D2/rinfo.cpp

## Purpose
Implements render state management classes for the WW3D2 engine, handling camera, fog, lighting, and material pass overrides.

## Responsibilities
- Manages render info state (fog, lighting, overrides)
- Handles material pass stack operations
- Provides special render info for specific render types
- Maintains reference counts for material passes

## Key Types
- RenderInfoClass (Class): Core render state container with camera, fog, and override flags
- SpecialRenderInfoClass (Class): Extended render info for special render types (e.g., post-processing)
- RINFO_OVERRIDE_FLAGS (Enum): Bit flags for render overrides (not shown in snippet)

## Key Functions
### Push_Material_Pass
- Purpose: Adds a material pass to the render stack
- Calls: `Add_Ref()`, `WWASSERT`

### Pop_Material_Pass
- Purpose: Removes the last material pass from the stack
- Calls: `Release_Ref()`, `WWASSERT`

### Push_Override_Flags
- Purpose: Pushes a new override flag set onto the stack
- Calls: `WWASSERT`

### Pop_Override_Flags
- Purpose: Pops the current override flag set
- Calls: `WWASSERT`

## Globals
- None

## Dependencies
- `rinfo.h`, `camera.h`, `matpass.h`
- `CameraClass`, `MaterialPassClass` (external)
- `WWASSERT` macro (assertion)
