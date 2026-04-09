# Generals/Code/Libraries/Source/WWVegas/WW3D2/texproject.cpp

## Purpose
Implements texture projection functionality for the SAGE engine, handling shadow mapping, light projections, and dynamic texture rendering.

## Responsibilities
- Manages texture projector state (intensity, attenuation, projection type)
- Computes perspective/orthographic projections for objects
- Handles render-to-texture operations for dynamic projections
- Updates projector parameters per frame
- Mainages bounding volumes for culling

## Key Types
- TexProjectClass (Class): Main texture projector implementation
- MaterialPassClass (Class): Material pass handling for projections
- VertexMaterialClass (Class): Vertex shader material for projections
- MatrixMapperClass (Class): Texture coordinate mapping

## Key Functions
### TexProjectClass::Compute_Perspective_Projection
- Purpose: Calculates perspective projection parameters for an object
- Calls: Set_Perspective_Projection, Set_Transform

### TexProjectClass::Compute_Ortho_Projection
- Purpose: Calculates orthographic projection parameters for an object
- Calls: Set_Ortho_Projection, Set_Transform

### TexProjectClass::Compute_Texture
- Purpose: Renders an object into a texture
- Calls: DX8Wrapper::Set_Render_Target, Configure_Camera, WW3D::Begin_Render, WW3D::Render, WW3D::End_Render

### TexProjectClass::Pre_Render_Update
- Purpose: Updates projector state before rendering
- Calls: Matrix3D::Multiply, Matrix4::Multiply, WW3D::Get_Frame_Time, MaterialPass->Peek_Material, Mapper->Set_Type, Mapper->Set_Texture_Transform

### TexProjectClass::Update_WS_Bounding_Volume
- Purpose: Recalculates world-space bounding box
- Calls: ProjectorClass::Update_WS_Bounding_Volume, WorldBoundingVolume.Compute_Axis_Aligned_Extent, Set_Cull_Box

## Globals
- INTENSITY_RATE_OF_CHANGE (float): Rate of intensity change per second (1.0f)

## Dependencies
- texproject.h, vertmaterial.h, shader.h, texture.h, rendobj.h, rinfo.h, camera.h, matpass.h, bwrender.h, assetmgr.h, dx8wrapper.h
- WW3D namespace, WWMath, Matrix3D, Matrix4, Vector3, AABoxClass, RenderObjClass, SpecialRenderInfoClass, CameraClass, TextureClass
