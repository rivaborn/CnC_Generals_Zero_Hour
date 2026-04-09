# Generals/Code/Libraries/Source/WWVegas/WW3D2/hrawanim.cpp

## Purpose
Handles loading and managing hierarchical animation data for the W3D engine.

## Responsibilities
- Loads animation data from W3D files
- Manages motion channels (translation, rotation, visibility)
- Interpolates animation data between frames
- Provides access to animation state for specific frames

## Key Types
- `NodeMotionStruct` (struct): Contains pointers to motion channels for a node
- `HRawAnimClass` (class): Main animation class handling loading and interpolation
- `MotionChannelClass` (class): Base class for animation channels (external)
- `BitChannelClass` (class): Base class for bit channels (external)

## Key Functions
### `HRawAnimClass::Load_W3D`
- Purpose: Loads animation data from a W3D file
- Calls: `Free`, `read_channel`, `read_bit_channel`, `add_channel`, `add_bit_channel`

### `HRawAnimClass::Get_Translation`
- Purpose: Returns the translation vector for a node at a specific frame
- Calls: `MotionChannelClass::Get_Vector`, `Vector3::Lerp`

### `HRawAnimClass::Get_Orientation`
- Purpose: Returns the orientation quaternion for a node at a specific frame
- Calls: `MotionChannelClass::Get_Vector`, `Fast_Slerp`

### `HRawAnimClass::Get_Transform`
- Purpose: Returns the full transform matrix for a node at a specific frame
- Calls: `MotionChannelClass::Get_Vector`, `Vector3::Lerp`, `Fast_Slerp`, `Build_Matrix3D`

### `HRawAnimClass::Get_Visibility`
- Purpose: Returns the visibility state for a node at a specific frame
- Calls: `BitChannelClass::Get_Bit`

## Globals
None

## Dependencies
- `hrawanim.h`, `motchan.h`, `chunkio.h`, `assetmgr.h`, `htree.h`
- `MotionChannelClass`, `BitChannelClass`, `HTreeClass`, `WW3DAssetManager`
- `Vector3`, `Quaternion`, `Matrix3D`, `WWMath`, `W3DNEW`, `W3DNEWARRAY`
