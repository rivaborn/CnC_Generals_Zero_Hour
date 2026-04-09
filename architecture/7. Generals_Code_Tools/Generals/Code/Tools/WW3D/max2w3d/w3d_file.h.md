# Generals/Code/Tools/WW3D/max2w3d/w3d_file.h

## Purpose
Defines the W3D file format structure and data types for 3D assets in Command & Conquer Generals.

## Responsibilities
- Declares chunk type enums for W3D file structure
- Defines data structures for meshes, materials, shaders, animations, and other 3D assets
- Provides versioning macros and naming conventions
- Includes obsolete chunk definitions

## Key Types
- W3dChunkHeader (Class): Basic chunk header structure
- W3dVectorStruct (Class): 3D vector representation
- W3dQuaternionStruct (Class): Quaternion for rotations
- W3dTexCoordStruct (Class): Texture coordinate structure
- W3dRGBStruct (Class): RGB color with operations
- W3dRGBAStruct (Class): RGBA color structure
- W3dMaterialInfoStruct (Class): Material information
- W3dVertexMaterialStruct (Class): Vertex material properties
- W3dShaderStruct (Class): Shader configuration
- W3dPS2ShaderStruct (Class): PS2-specific shader settings
- W3dTextureInfoStruct (Class): Texture parameters
- W3dTriStruct (Class): Triangle definition
- W3dMeshHeader3Struct (Class): Mesh header information
- W3dVertInfStruct (Class): Vertex influence data
- W3dMeshDeform (Class): Mesh deformation information
- W3dDeformSetInfo (Class): Deformation set data
- W3dDeformKeyframeInfo (Class): Deformation keyframe
- W3dDeformData (Class): Per-vertex deformation data
- W3dMeshAABTreeHeader (Class): AABTree header
- W3dMeshAABTreeNode (Class): AABTree node
- W3dHierarchyStruct (Class): Hierarchy node
- W3dPivotStruct (Class): Pivot point
- W3dPivotFixupStruct (Class): Pivot fixup data
- W3dAnimHeaderStruct (Class): Animation header
- W3dCompressedAnimHeaderStruct (Class): Compressed animation header
- W3dAnimChannelStruct (Class): Animation channel
- W3dBitChannelStruct (Class): Bit channel for animations
- W3dTimeCodedAnimChannelStruct (Class): Time-coded animation channel
- W3dTimeCodedBitChannelStruct (Class): Time-coded bit channel
- W3dAdaptiveDeltaAnimChannelStruct (Class): Adaptive delta animation channel
- W3dMorphAnimHeaderStruct (Class): Morph animation header
- W3dMorphAnimKeyStruct (Class): Morph animation key
- W3dHModelHeaderStruct (Class): Hierarchical model header
- W3dHModelNodeStruct (Class): Hierarchical model node
- W3dLODModelHeaderStruct (Class): LOD model header
- W3dLODStruct (Class): LOD definition
- W3dCollectionHeaderStruct (Class): Collection header
- W3dPlaceholderStruct (Class): Placeholder object
- W3dTransformNodeStruct (Class): Transform node
- W3dLightStruct (Class): Light properties
- W3dSpotLightStruct (Class): Spot light properties
- W3dLightAttenuationStruct (Class): Light attenuation
- W3dLightTransformStruct (Class): Light transform
- W3dEmitterHeaderStruct (Class): Particle emitter header
- W3dEmitterUserInfoStruct (Class): Emitter user data
- W3dEmitterInfoStruct (Class): Emitter properties
