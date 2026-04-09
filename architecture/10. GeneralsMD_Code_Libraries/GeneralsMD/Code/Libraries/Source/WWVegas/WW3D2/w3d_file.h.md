# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3d_file.h

## Purpose
Defines the file format structures and chunk types for W3D (Westwood 3D) assets used in the game engine.

## Responsibilities
- Defines chunk ID enums for all W3D object types
- Declares data structures for meshes, hierarchies, animations, materials, shaders, etc.
- Provides version macros and naming conventions
- Includes obsolete chunk definitions

## Key Types
- W3dChunkHeader (Class): Base chunk header structure
- W3dVectorStruct (Class): 3D vector representation
- W3dShaderStruct (Class): Shader configuration structure
- W3dMeshHeader3Struct (Class): Mesh header information
- W3dMaterialInfoStruct (Class): Material information
- W3dTextureInfoStruct (Class): Texture information
- W3dTriStruct (Class): Triangle definition
- W3dRGBStruct (Class): RGB color structure
- W3dRGBAStruct (Class): RGBA color structure
- W3dVertexMaterialStruct (Class): Vertex material properties
- W3dTexCoordStruct (Class): Texture coordinate structure
- W3dQuaternionStruct (Class): Quaternion rotation representation
- W3dMeshAABTreeHeader (Class): Axis-Aligned Bounding Tree header
- W3dMeshAABTreeNode (Class): AABTree node structure
- W3dHierarchyStruct (Class): Hierarchy node structure
- W3dPivotStruct (Class): Pivot point definition
- W3dAnimHeaderStruct (Class): Animation header
- W3dCompressedAnimHeaderStruct (Class): Compressed animation header
- W3dAnimChannelStruct (Class): Animation channel data
- W3dBitChannelStruct (Class): Bit channel animation data
- W3dTimeCodedAnimChannelStruct (Class): Time-coded animation channel
- W3dAdaptiveDeltaAnimChannelStruct (Class): Adaptive delta animation channel
- W3dMorphAnimHeaderStruct (Class): Morph animation header
- W3dHModelHeaderStruct (Class): Hierarchical model header
- W3dHModelNodeStruct (Class): Hierarchical model node
- W3dLODModelHeaderStruct (Class): LOD model header
- W3dLODStruct (Class): LOD definition
- W3dCollectionHeaderStruct (Class): Collection header
- W3dPlaceholderStruct (Class): Placeholder object
- W3dTransformNodeStruct (Class): Transform node
- W3dLightStruct (Class): Light definition
- W3dSpotLightStruct (Class): Spot light definition
- W3dLightAttenuationStruct (Class): Light attenuation
- W3dLightTransformStruct (Class): Light transform
- W3dEmitterHeaderStruct (Class): Particle emitter header
- W3dEmitterInfoStruct (Class): Emitter properties
- W3dEmitterExtraInfoStruct (Class): Additional emitter info
- W3dEmitterInfoStructV2 (Class): Version 2 emitter info
- W3dEmitterPropertyStruct (Class): Emitter property
- W3dEmitterLinePropertiesStruct (Class): Line emitter properties
- W3dAggregateHeaderStruct (Class): Aggregate header
- W3dAggregateInfoStruct (Class): Aggregate information
- W3dTextureReplacerHeaderStruct (Class): Texture replacer header
- W3dTextureReplacerStruct (Class): Texture replacement data
- W3dAggregateMiscInfo (Class): Aggregate miscellaneous info
- W3dHLodHeaderStruct (Class): HLOD
