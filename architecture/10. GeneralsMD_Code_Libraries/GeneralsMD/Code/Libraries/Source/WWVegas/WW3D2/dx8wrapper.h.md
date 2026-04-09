# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8wrapper.h

## Purpose
Header file defining the DX8Wrapper class, a Direct3D 8 wrapper for the SAGE engine, managing rendering states, resources, and device interactions.

## Responsibilities
- Encapsulates Direct3D 8 device management
- Tracks render state changes (matrices, textures, materials, etc.)
- Provides resource creation and management (textures, buffers)
- Handles scene rendering and device state validation
- Supports deferred state application for optimization

## Key Types
- **DX8Wrapper (Class)**: Main wrapper for Direct3D 8 device operations
- **RenderStateStruct (Class)**: Stores current render state (matrices, textures, lights, etc.)
- **ChangedStates (Enum)**: Bit flags for tracking state changes
- **BUFFER_TYPE_DX8 (Enum)**: Buffer type identifiers
- **DX8_CleanupHook (Class)**: Interface for resource cleanup during device reset

## Key Functions
### `Set_Render_State`
- Purpose: Applies a complete render state configuration
- Calls: `Add_Engine_Ref`, `Release_Engine_Ref`

### `Apply_Render_State_Changes`
- Purpose: Applies deferred render state changes before drawing
- Calls: Not inferable (internal implementation)

### `Draw_Triangles`
- Purpose: Renders triangle primitives with specified parameters
- Calls: `Apply_Render_State_Changes`, `Draw_Sorting_IB_VB`

### `Set_Texture`
- Purpose: Binds a texture to a texture stage
- Calls: `REF_PTR_SET`

## Globals
- `MAX_TEXTURE_STAGES (unsigned)`: Maximum texture stages supported
- `MAX_VERTEX_STREAMS (unsigned)`: Maximum vertex streams
- `number_of_DX8_calls (unsigned)`: Counter for DX8 API calls
- `_DX8SingleThreaded (bool)`: Flag for single-threaded DX8 usage

## Dependencies
- Direct3D 8 headers (`d3d8.h`)
- Engine-specific headers (`matrix4.h`, `shader.h`, `texture.h`)
- Utility headers (`dllist.h`, `wwstring.h`)
- Platform-specific headers (`always.h`, `cpudetect.h`)
