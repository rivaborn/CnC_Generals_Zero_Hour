# Generals/Code/Tools/WW3D/max2w3d/w3d_obsolete.h

## Purpose
Header file defining obsolete W3D (Westwood 3D) chunk IDs and data structures for mesh and material formats.

## Responsibilities
- Defines deprecated chunk IDs for W3D file format
- Provides obsolete material and mesh data structures
- Documents retired features and formats

## Key Types
- (anonymous enum) (Enum): obsolete chunk ID values
- W3dMaterialStruct (Struct): version 1.0 material data
- W3dMaterial2Struct (Struct): version 2.0 material data
- W3dMaterial3Struct (Struct): version 3.0 material data
- W3dMap3Struct (Struct): texture map data
- W3dSurrenderTriStruct (Struct): triangle data
- W3dMeshHeaderStruct (Struct): mesh header data
- W3dMeshDamageStruct (Struct): mesh damage data
- W3dHModelAuxDataStruct (Struct): retired HModel auxiliary data

## Key Functions
None

## Globals
None

## Dependencies
- W3D_NAME_LEN, W3dRGBStruct, W3dTexCoordStruct, W3dVectorStruct (external types)
- Standard types: uint32, uint16, uint8, float32, char
