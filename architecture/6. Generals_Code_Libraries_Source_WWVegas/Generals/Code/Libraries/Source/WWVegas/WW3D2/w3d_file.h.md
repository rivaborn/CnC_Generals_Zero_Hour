# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3d_file.h

## Purpose
Defines the W3D file format structures and chunk types for the SAGE engine's 3D rendering system.

## Responsibilities
- Declares chunk ID enums for all W3D file components
- Defines data structures for meshes, hierarchies, animations, materials, shaders, etc.
- Specifies versioning and naming conventions for W3D assets
- Provides structs for emitters, aggregates, HLODs, collision boxes, and sound objects

## Key Types
- W3dChunkHeader (Class): Base chunk header structure
- W3dVectorStruct (Class): 3D vector representation
- W3dQuaternionStruct (Class): Quaternion for rotations
- W3dTexCoordStruct (Class): Texture coordinate structure
- W3dRGBStruct (Class): RGB color with operations
- W3dRGBAStruct (Class): RGBA color with alpha
- W3dMaterialInfoStruct (Class): Material information
- W3dVertexMaterialStruct (Class): Vertex material properties
- W3dShaderStruct (Class): Shader configuration
- W3dPS2ShaderStruct (Class): PS2-specific shader settings
- W3dTextureInfoStruct (Class): Texture parameters
- W3dTriStruct (Class): Triangle definition
- W3dMeshHeader3Struct (Class): Mesh header v3
- W3dMeshAABTreeHeader (Class): AABTree header
- W3dMeshAABTreeNode (Class): AABTree node
- W3dHierarchyStruct (Class): Hierarchy node
- W3dPivotStruct (Class): Pivot point
- W3dAnimHeaderStruct (Class): Animation header
- W3dEmitterInfoStruct (Class): Particle emitter properties
- W3dAggregateHeaderStruct (Class): Aggregate header
- W3dHLodHeaderStruct (Class): HLOD header
- W3dBoxStruct (Class): Collision box
- W3dNullObjectStruct (Class): Null object
- W3dSoundRObjHeaderStruct (Class): Sound object header

## Key Functions
### W3d_Vertex_Material_Reset
- Purpose: Reset vertex material to defaults
- Calls: None

### W3d_Shader_Reset
- Purpose: Reset shader to default state
- Calls: None

### W3d_Shader_Set_Depth_Compare
- Purpose: Set shader depth comparison function
- Calls: None

### W3d_Shader_Set_Depth_Mask
- Purpose: Set shader depth mask
- Calls: None

### W3d_Shader_Set_Dest_Blend_Func
- Purpose: Set destination blend function
- Calls: None

### W3d_Shader_Set_Pri_Gradient
- Purpose: Set primary gradient mode
- Calls: None

### W3d_Shader_Set_Sec_Gradient
- Purpose: Set secondary gradient mode
- Calls: None

### W3d_Shader_Set_Src_Blend_Func
- Purpose: Set source blend function
- Calls: None

### W3d_Shader_Set_Texturing
- Purpose: Enable/disable texturing
- Calls: None

### W3d_Shader_Set_Detail_Color_Func
- Purpose: Set detail color function
- Calls: None

### W3d_Shader_Set_Detail_Alpha_Func
- Purpose: Set detail alpha function
- Calls: None

### W3d_Shader_Set_Alpha_Test
- Purpose: Enable/disable alpha testing
-
