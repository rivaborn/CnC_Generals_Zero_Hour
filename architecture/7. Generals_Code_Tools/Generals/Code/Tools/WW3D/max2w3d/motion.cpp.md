# Generals/Code/Tools/WW3D/max2w3d/motion.cpp

## Purpose
Handles animation data extraction from 3D Studio Max and conversion to W3D format for the game engine.

## Responsibilities
- Captures node transformations across animation frames
- Computes motion deltas between base pose and animated frames
- Saves animation data in W3D format (compressed or uncompressed)
- Manages visibility and movement flags per node/frame

## Key Types
- **MotionClass**: Main class handling animation capture and export
- **BooleanVectorClass**: Stores visibility/movement flags per frame
- **W3dAnimHeaderStruct/W3dCompressedAnimHeaderStruct**: Animation metadata structures

## Key Functions
### MotionClass::compute_frame_motion
- Purpose: Captures node transformations for a specific frame
- Calls: HierarchySaveClass constructor, BasePose methods, set_motion_matrix

### MotionClass::Save
- Purpose: Exports animation data to W3D file format
- Calls: save_header, save_channels, ChunkSaveClass methods

### MotionClass::save_channels
- Purpose: Writes per-node animation channels (translation/rotation)
- Calls: VectorChannelClass/BitChannelClass Save methods

## Globals
- **ExportLog**: Logging utility (external)
- **W3D_CHUNK_* constants**: Chunk type identifiers (external)

## Dependencies
- motion.h, w3d_file.h, vchannel.h, bchannel.h, euler.h, util.h
- errclass.h, w3dutil.h, exportlog.h
- 3DS Max SDK types (IScene, INode, etc.)
