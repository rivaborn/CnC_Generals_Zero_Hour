# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3d_obsolete.h

## Purpose
Defines obsolete W3D (Westwood 3D) file format structures and chunk IDs for backward compatibility.

## Responsibilities
- Declares deprecated chunk IDs for mesh, material, and damage data.
- Defines obsolete material and mesh header structures.
- Provides legacy damage and auxiliary model data structures.

## Key Types
- (anonymous enum) (Enum): obsolete chunk ID values.
- W3dMaterialStruct (Struct): version 1 material definition.
- W3dMaterial2Struct (Struct): version 2 material with animation support.
- W3dMaterial3Struct (Struct): version 3 material with advanced rendering attributes.
- W3dMap3Struct (Struct): texture map parameters.
- W3dSurrenderTriStruct (Struct): triangle with texture coordinates and normals.
- W3dMeshHeaderStruct (Struct): original mesh header with counts and bounds.
- W3dMeshDamageStruct (Struct): mesh damage description.
- W3dMeshDamageVertexStruct (Struct): modified vertex data.
- W3dMeshDamageColorStruct (Struct): modified vertex color data.
- W3dHModelAuxDataStruct (Struct): retired hierarchy model auxiliary data.

## Key Functions
None.

## Globals
None.

## Dependencies
- Uses `W3D_NAME_LEN`, `W3dRGBStruct`, `W3dTexCoordStruct`, `W3dVectorStruct` from other headers.
- Defines material attribute and mapping type constants.
