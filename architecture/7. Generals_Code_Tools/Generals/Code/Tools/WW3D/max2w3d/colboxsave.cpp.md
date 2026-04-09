# Generals/Code/Tools/WW3D/max2w3d/colboxsave.cpp

## Purpose
Handles exporting collision box data from 3ds Max to W3D format for game assets.

## Responsibilities
- Extracts mesh data from 3ds Max scene nodes
- Computes axis-aligned or oriented bounding boxes
- Sets collision attributes based on node properties
- Writes collision data to W3D file chunks

## Key Types
- **CollisionBoxSaveClass (Class)**: Manages collision box export process
- **BoxData (struct)**: Stores collision box parameters (center, extent, attributes)

## Key Functions
### CollisionBoxSaveClass constructor
- Purpose: Initializes collision box data from 3ds Max node
- Calls: `inode->EvalWorldState()`, `obj->ConvertToType()`, `Is_Collision_AABox()`, `Is_Physical_Collision()`, etc.

### Write_To_File
- Purpose: Writes collision box data to W3D file
- Calls: `csave.Begin_Chunk()`, `csave.Write()`, `csave.End_Chunk()`

## Globals
- None

## Dependencies
- `colboxsave.h`, `w3d_file.h`, `util.h`, `w3dappdata.h`, `errclass.h`
- 3ds Max SDK types: `INode`, `Matrix3`, `TimeValue`, `Object`, `TriObject`, `Mesh`
- W3D constants: `W3D_BOX_CURRENT_VERSION`, `W3D_CHUNK_BOX`, collision attribute flags
