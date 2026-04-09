# Generals/Code/Libraries/Source/WWVegas/WW3D2/dazzle.h

## Purpose
Header file defining classes for dazzle (light lens flare) effects in the 3D rendering system.

## Responsibilities
- Declares dazzle effect types, layers, and rendering objects
- Defines initialization structures for dazzle and lens flare effects
- Provides visibility handling and prototype loading infrastructure

## Key Types
- **DazzleInitClass (Class)**: Dazzle effect initialization parameters
- **LensflareInitClass (Class)**: Lens flare effect initialization parameters
- **DazzleTypeClass (Class)**: Manages dazzle effect types and shaders
- **DazzleLayerClass (Class)**: Manages dazzle rendering layers per scene
- **LensflareTypeClass (Class)**: Manages lens flare effect types
- **DazzleRenderObjClass (Class)**: Renderable dazzle object in the scene
- **DazzleVisibilityClass (Class)**: Abstract base for visibility testing
- **DazzlePrototypeClass (Class)**: Prototype for loading dazzle assets
- **DazzleLoaderClass (Class)**: Asset loader for dazzle prototypes

## Key Functions
### DazzleTypeClass::Calculate_Intensities
- Purpose: Computes dazzle/halo intensities based on camera position
- Calls: None visible

### DazzleLayerClass::Render
- Purpose: Renders all dazzles in this layer
- Calls: None visible

### LensflareTypeClass::Generate_Vertex_Buffers
- Purpose: Generates vertex data for lens flare rendering
- Calls: None visible

### DazzleRenderObjClass::Render
- Purpose: Renders the dazzle effect
- Calls: Render_Dazzle, vis_render_dazzle

### DazzleRenderObjClass::Set_Current_Dazzle_Layer
- Purpose: Sets the active dazzle layer for rendering
- Calls: None visible

## Globals
- **_DazzleLoader (DazzleLoaderClass)**: Global instance for loading dazzle assets

## Dependencies
- "vector3.h", "matrix3d.h", "rendobj.h", "wwstring.h", "proto.h", "w3derr.h", "shader.h", "matrix4.h"
- CameraClass, TextureClass, ShaderClass, INIClass, RenderInfoClass, SpecialRenderInfoClass, SphereClass, AABoxClass
