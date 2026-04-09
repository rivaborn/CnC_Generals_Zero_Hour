# Generals/Code/Tools/WW3D/max2w3d/motion.h

## Purpose
Defines the MotionClass for handling animation data export from 3DS Max to W3D format.

## Responsibilities
- Manages motion data for nodes across animation frames
- Handles visibility and binary movement flags per node/frame
- Computes frame motion and stores matrices/euler angles
- Saves motion data to W3D chunks

## Key Types
- **W3dExportOptionsStruct (Class)**: Not inferable.
- **MotionClass (Class)**: Handles animation export logic and data storage.

## Key Functions
### MotionClass (Constructor)
- Purpose: Initializes motion data for single root node or node list.
- Calls: Not inferable.

### ~MotionClass (Destructor)
- Purpose: Cleans up motion data.
- Calls: Not inferable.

### Save
- Purpose: Saves motion data to a chunk stream.
- Calls: save_header, save_channels.

### compute_frame_motion
- Purpose: Computes motion data for a specific frame.
- Calls: Not inferable.

### set_motion_matrix / get_motion_matrix
- Purpose: Sets/gets motion matrix for a node at a frame.
- Calls: Not inferable.

### set_eulers / get_eulers
- Purpose: Sets/gets euler angles for a node at a frame.
- Calls: Not inferable.

### set_visibility / get_visibility
- Purpose: Sets/gets visibility flag for a node at a frame.
- Calls: Not inferable.

### set_binary_movement / get_binary_movement
- Purpose: Sets/gets binary movement flag for a node at a frame.
- Calls: Not inferable.

### save_header / save_channels
- Purpose: Saves motion header/channel data to W3D chunks.
- Calls:
