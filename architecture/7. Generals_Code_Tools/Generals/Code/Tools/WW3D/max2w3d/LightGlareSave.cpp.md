# Generals/Code/Tools/WW3D/max2w3d/LightGlareSave.cpp

## Purpose
Handles saving light glare data for 3D models in the Max2W3D conversion tool.

## Responsibilities
- Constructs light glare data from 3DS Max scene nodes
- Writes light glare data to W3D file chunks
- Manages position transformation for glare effects

## Key Types
- `LightGlareSaveClass` (Class): Manages light glare data export
- `GlareData` (Struct): Stores glare position and properties

## Key Functions
### `LightGlareSaveClass::LightGlareSaveClass`
- Purpose: Initializes light glare data from 3DS Max node
- Calls: `memset`, `GetObjectTM`, `Inverse`

### `LightGlareSaveClass::Write_To_File`
- Purpose: Writes glare data to W3D file chunks
- Calls: `Begin_Chunk`, `Write`, `End_Chunk`

## Globals
None

## Dependencies
- `LightGlareSave.h`
- `w3d_file.h`
- `util.h`
- `w3dappdata.h`
- `errclass.h`
- 3DS Max SDK types (`INode`, `Matrix3`, `TimeValue`)
