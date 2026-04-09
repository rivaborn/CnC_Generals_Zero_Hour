# Generals/Code/Libraries/Source/WWVegas/WW3D2/line3d.cpp

## Purpose
Implements a 3D line rendering object using a box model with 8 vertices and 12 triangles.

## Responsibilities
- Constructs and renders 3D lines with configurable width, color, and opacity
- Manages line transformations and bounding volumes
- Handles line scaling, resetting, and color/opacity updates

## Key Types
- **Line3DClass (Class)**: Represents a 3D line renderable object
- **Indices (const unsigned short[36])**: Predefined triangle indices for the line's box model

## Key Functions
### Line3DClass::Line3DClass
- Purpose: Constructs a 3D line with start/end points, width, and color
- Calls: Matrix3D::Obj_Look_At, Set_Transform

### Line3DClass::Render
- Purpose: Renders the 3D line using DirectX8 vertex/index buffers
- Calls: WW3D::Add_To_Static_Sort_List, DX8Wrapper::Set_Shader, DX8Wrapper::Set_Texture, DX8Wrapper::Set_Material, DX8Wrapper::Set_Transform, DX8Wrapper::Set_Vertex_Buffer, DX8Wrapper::Set_Index_Buffer, DX8Wrapper::Draw_Triangles

### Line3DClass::Scale
- Purpose: Scales the line uniformly or non-uniformly
- Calls: Invalidate_Cached_Bounding_Volumes, Get_Container, Update_Obj_Space_Bounding_Volumes

### Line3DClass::Reset
- Purpose: Resets line start/end points and optionally width
- Calls: Scale, Matrix3D::Obj_Look_At, Set_Transform, Invalidate_Cached_Bounding_Volumes, Get_Container, Update_Obj_Space_Bounding_Volumes

### Line3DClass::Re_Color
- Purpose: Updates the line's color
- Calls: None

### Line3DClass::Set_Opacity
- Purpose: Sets line opacity and configures shader/sort level
- Calls: Set_Sort_Level

## Globals
- **Indices (const unsigned short[36])**: Triangle indices for the line's box model

## Dependencies
- line3d.h, vertmaterial.h, shader.h, wwdebug.h, ww3d.h, rinfo.h, dx8wrapper.h, dx8vertexbuffer.h, dx8indexbuffer.h, dx8fvf.h
- RenderObjClass, Vector3, Vector4, Matrix3D, SphereClass, AABoxClass, RenderInfoClass, VertexMaterialClass, ShaderClass, DynamicVBAccessClass, DynamicIBAccessClass, FVFInfoClass
