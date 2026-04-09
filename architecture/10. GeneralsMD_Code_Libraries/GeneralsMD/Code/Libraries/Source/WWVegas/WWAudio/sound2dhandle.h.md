# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/sound2dhandle.h

## Purpose
Defines the `Sound2DHandleClass` for managing 2D audio samples in the game's audio system.

## Responsibilities
- Wraps a Miles Sound System (MSS) 2D sample handle (`HSAMPLE`).
- Provides methods to control playback (start, stop, resume, end).
- Manages sample properties (volume, pan, loop count, playback rate).
- Inherits from `SoundHandleClass` for base functionality.

## Key Types
- **Sound2DHandleClass (Class)**: Wrapper for 2D audio sample handles with playback control.

## Key Functions
### `Sound2DHandleClass()`
- Purpose: Default constructor.
- Calls: None.

### `~Sound2DHandleClass()`
- Purpose: Destructor.
- Calls: None.

### `Get_HSAMPLE()`
- Purpose: Returns the underlying MSS sample handle.
- Calls: None.

### `Set_Miles_Handle(uint32 handle)`
- Purpose: Sets the MSS sample handle.
- Calls: None.

### `Initialize(SoundBufferClass *buffer)`
- Purpose: Initializes the sample with a sound buffer.
- Calls: None.

### `Start_Sample()`
- Purpose: Starts playback of the sample.
- Calls: None.

### `Stop_Sample()`
- Purpose: Stops playback of the sample.
- Calls: None.

### `Resume_Sample()`
- Purpose: Resumes playback of a stopped sample.
- Calls: None.

### `End_Sample()`
- Purpose: Ends playback of the sample.
- Calls: None.

### `Set_Sample_Pan(S32 pan)`
- Purpose: Sets the pan (left/right balance) of the sample.
- C
