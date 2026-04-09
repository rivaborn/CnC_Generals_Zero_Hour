# Generals/Code/Libraries/Source/WWVegas/WWAudio/sound3dhandle.h

## Purpose
Defines the `Sound3DHandleClass` for managing 3D audio samples in the game's audio system.

## Responsibilities
- Wraps a 3D audio sample handle (`H3DSAMPLE`) for spatial audio control.
- Provides methods to manipulate 3D sound properties (pan, volume, playback rate).
- Inherits from `SoundHandleClass` for base audio functionality.
- Exposes Miles Sound System (MSS) 3D sample operations.

## Key Types
- **Sound3DHandleClass (Class)**: Wrapper for 3D audio sample handles with spatial control methods.

## Key Functions
### `Sound3DHandleClass()`
- Purpose: Default constructor.
- Calls: None.

### `~Sound3DHandleClass()`
- Purpose: Destructor.
- Calls: None.

### `Get_H3DSAMPLE()`
- Purpose: Returns the underlying 3D sample handle.
- Calls: None.

### `Set_Miles_Handle(uint32 handle)`
- Purpose: Sets the Miles Sound System handle.
- Calls: None.

### `Initialize(SoundBufferClass *buffer)`
- Purpose: Initializes the 3D sample with a sound buffer.
- Calls: None.

### `Start_Sample()`
- Purpose: Starts playback of the 3D sample.
- Calls: None.

### `Stop_Sample()`
- Purpose: Stops playback of the 3D sample.
- Calls: None.

### `Resume_Sample()`
- Purpose: Resumes playback of a stopped 3D sample.
- Calls: None.

### `End_Sample()`
- Purpose: Ends playback of the 3D sample.
- Calls: None.

### `Set_Sample_Pan(S3
