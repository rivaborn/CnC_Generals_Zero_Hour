# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texproject.cpp

## Purpose
Implements texture projection functionality for the SAGE engine, handling shadow mapping, light projections, and dynamic texture rendering.

## Responsibilities
- Manages texture projector state (intensity, attenuation, projection type)
- Computes perspective/orthographic projections for objects
- Generates textures by rendering objects to render targets
- Updates projector parameters before rendering
- Handles intensity interpolation and culling

## Key Types
- **TexProjectClass**: Main texture projector class handling projection rendering
- **MaterialPassClass**: Material pass configuration for the projector
- **MatrixMapperClass**: Texture coordinate mapping for projections

## Key Functions
### TexProjectClass::Compute_Texture
- Purpose: Renders an object to generate a texture
- Calls: Configure_Camera, WW3D::Begin_Render, WW3D::Render, WW3D::End_Render

### TexProjectClass::Pre_Render_Update
- Purpose: Updates projector state before rendering
- Calls: WW3D::Get_Frame_Time, MaterialPass->Peek_Material, Mapper->Set_Texture_Transform

### TexProjectClass::Configure_Camera
- Purpose: Configures camera parameters to match projector settings
- Calls: CameraClass::Set_Transform, CameraClass::Set_Clip_Planes

## Globals
- **INTENSITY_RATE_OF_CHANGE (float)**: Rate of intensity change per second (1.0f)

## Dependencies
- Key includes: "texproject.h", "vertmaterial.h", "shader.h", "texture.h", "rendobj.h", "rinfo.h", "camera.h", "matpass.h", "bwrender.h", "assetmgr.h", "dx8wrapper.h"
- External symbols: WW3D::Get_Frame_Time, WW3D::Begin_Render, WW3D::Render, WW3D::End_Render, DX8Wrapper::Set_Render_Target_With_Z
