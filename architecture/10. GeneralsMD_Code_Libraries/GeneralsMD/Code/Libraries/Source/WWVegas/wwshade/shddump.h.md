# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddump.h

## Purpose
Header file for the wdump utility, providing shader chunk definitions and class IDs.

## Responsibilities
- Defines shader chunk structure (`ShdDef_ChunkStruct`)
- Provides shader class ID strings (`Shader_ClassIDs`)
- Includes shader class ID definitions

## Key Types
- **ShdDef_ChunkStruct (struct)**: Represents a shader chunk with ID, name, surface type, and texture name.
- **Shader_ClassIDs (array)**: Maps shader class IDs to their string names.

## Key Functions
None.

## Globals
- **Shader_ClassIDs (const char\*)**: Array mapping shader class IDs to their string names.

## Dependencies
- `shdclassids.h` (included)
