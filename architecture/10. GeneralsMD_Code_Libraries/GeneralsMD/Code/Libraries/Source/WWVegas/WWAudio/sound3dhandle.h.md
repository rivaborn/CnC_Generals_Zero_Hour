# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/sound3dhandle.h

## Purpose
Defines the `Sound3DHandleClass` for managing 3D audio samples in the game engine.

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

### `Start_Sample()`, `Stop_Sample()`, `Resume_Sample()`, `End_Sample()`
- Purpose: Controls playback state of the 3D sample.
- Calls: None.

### `Set_Sample_Pan(S32 pan)`, `Get_Sample_Pan()`
- Purpose: Sets/gets the stereo pan of the 3D sample.
- Calls: None.

### `Set_Sample_Volume(S32 volume)`, `Get_Sample_Volume()`
- Purpose: Sets/gets the volume of the
