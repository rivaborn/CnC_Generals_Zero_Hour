# Generals/Code/Tools/WW3D/max2w3d/dazzlesave.cpp

## Purpose
Handles saving dazzle (special effect) data from 3DS Max to W3D format.

## Responsibilities
- Constructs dazzle save object with mesh and container names
- Extracts dazzle type from node app data
- Writes dazzle chunk data to output file

## Key Types
- DazzleSaveClass (Class): manages dazzle effect export
- W3DDazzleAppDataStruct (Struct): holds dazzle type data

## Key Functions
### DazzleSaveClass constructor
- Purpose: Initializes dazzle save object with node data
- Calls: `W3DDazzleAppDataStruct::Get_App_Data`

### Write_To_File
- Purpose: Writes dazzle chunk data to output file
- Calls: `csave.Begin_Chunk`, `csave.Write`, `csave.End_Chunk`

## Globals
None

## Dependencies
- `dazzlesave.h`, `w3d_file.h`, `util.h`, `w3dappdata.h`, `errclass.h`
- `W3D_CHUNK_DAZZLE`, `W3D_CHUNK_DAZZLE_NAME`, `W3D_CHUNK_DAZZLE_TYPENAME`
