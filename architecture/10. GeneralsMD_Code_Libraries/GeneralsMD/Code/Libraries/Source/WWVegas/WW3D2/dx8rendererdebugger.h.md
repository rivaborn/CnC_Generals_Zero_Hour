# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8rendererdebugger.h

## Purpose
Header for a debug utility class that manages rendering debug information in the DirectX 8 renderer.

## Responsibilities
- Controls debug rendering enable/disable state
- Manages debug mesh rendering
- Provides debug string output
- Handles per-frame debug updates

## Key Types
- StringClass (Class): Not inferable (forward declaration)
- MeshClass (Class): Not inferable (forward declaration)
- DX8RendererDebugger (Class): Main debugger class with static methods for debug rendering control

## Key Functions
### Enable
- Purpose: Enable or disable the debug renderer
- Calls: None

### Is_Enabled
- Purpose: Check if debug rendering is enabled
- Calls: None

### Get_String
- Purpose: Retrieve debug information as a string
- Calls: None

### Update
- Purpose: Update debug rendering state each frame
- Calls: None

### Add_Mesh
- Purpose: Add a mesh to debug rendering (only in debug builds)
- Calls: None

### Disable_Mesh
- Purpose: Disable debug rendering for a specific mesh
- Calls: None

### Enable_Mesh
- Purpose: Enable debug rendering for a specific mesh
- Calls: None

### Disable_All
- Purpose: Disable debug rendering for all meshes
- Calls: None

### Enable_All
- Purpose: Enable debug rendering for all meshes
- Calls: None

## Globals
- Enabled (bool): Static flag tracking debug renderer state

## Dependencies
- "always.h" (include)
- StringClass (forward declaration)
- MeshClass (forward declaration)
