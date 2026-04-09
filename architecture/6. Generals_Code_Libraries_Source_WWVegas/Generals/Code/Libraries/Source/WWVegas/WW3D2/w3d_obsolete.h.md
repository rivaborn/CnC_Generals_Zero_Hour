# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3d_obsolete.h

## Purpose
Defines obsolete W3D (Westwood 3D) chunk IDs, material structures, and mesh data formats that are no longer used in the current engine version.

## Responsibilities
- Declares deprecated chunk identifiers for 3D model data
- Defines obsolete material structures (v1, v2, v3)
- Specifies retired mesh header and damage structures
- Provides legacy mapping and rendering attribute definitions

## Key Types
- W3dMaterialStruct (Struct): Version 1 material definition
- W3dMaterial2Struct (Struct): Version 2 material with animation support
- W3dMaterial3Struct (Struct): Version 3 material with advanced rendering attributes
- W3dMap3Struct (Struct): Texture map definition
- W3dMeshHeaderStruct (Struct): Original mesh header format
- W3dMeshDamageStruct (Struct): Mesh damage description
- W3dHModelAuxDataStruct (Struct): Retired hierarchy model auxiliary data

## Key Functions
None

## Globals
None

## Dependencies
- W3D_NAME_LEN (macro)
- W3dRGBStruct (struct)
- W3dTexCoordStruct (struct)
- W3dVectorStruct (struct)
