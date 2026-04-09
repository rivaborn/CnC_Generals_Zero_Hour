# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dazzle.h

## Purpose
Defines classes and interfaces for dazzle (lighting/flare) effects in the 3D rendering system.

## Responsibilities
- Declares dazzle effect types, layers, and rendering objects
- Manages lens flare effects and visibility handling
- Provides initialization and loading infrastructure for dazzle assets
- Defines prototype system for dazzle objects in W3D files

## Key Types
- **DazzleTypeClass (Class)**: Manages dazzle effect parameters and shaders
- **DazzleLayerClass (Class)**: Handles rendering of dazzles with specific camera settings
- **DazzleRenderObjClass (Class)**: Renderable dazzle object with visibility and transformation
- **LensflareTypeClass (Class)**: Manages lens flare effect parameters and rendering
- **DazzleVisibilityClass (Class)**: Abstract base for custom visibility calculations
- **DazzlePrototypeClass (Class)**: W3D prototype for dazzle objects
- **DazzleLoaderClass (Class)**: Asset loader for dazzle chunks in W3D files
- **DazzleInitClass (Class)**: Initialization parameters for dazzle effects
- **LensflareInitClass (Class)**: Initialization parameters for lens flares
- **VertexFormatXYZNDUV2 (Struct)**: Vertex format for dazzle rendering

## Key Functions
### `Calculate_Intensities`
- Purpose: Computes dazzle and halo intensities based on camera/dazzle positions
- Calls: None visible

### `Render`
- Purpose: Renders dazzle effects and manages visibility lists
- Calls: `Render_Dazzle`, `vis_render_dazzle`

### `Set_Current_Dazzle_Layer`
- Purpose: Sets the active dazzle layer for rendering
- Calls: None visible

### `Init_Type`
- Purpose: Registers a new dazzle type
- Calls: None visible

### `Init_Lensflare`
- Purpose: Registers a new lens flare type
- Calls: None visible

## Globals
- **_DazzleLoader (DazzleLoaderClass)**: Global instance for loading dazzle assets

## Dependencies
- `always.h`, `vector3.h`, `matrix3d.h`, `rendobj.h`, `wwstring.h`, `proto.h`, `w3derr.h`, `shader.h`, `matrix4.h`
- `CameraClass`, `DazzleVisibilityClass`, `VertexFormatXYZNDUV2`, `INIClass`, `TextureClass`, `ShaderClass`, `RenderInfoClass`, `SpecialRenderInfoClass`, `ChunkLoadClass`, `PrototypeClass`, `W
