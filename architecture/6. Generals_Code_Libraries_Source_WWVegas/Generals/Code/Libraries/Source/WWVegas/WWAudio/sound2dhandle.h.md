# Generals/Code/Libraries/Source/WWVegas/WWAudio/sound2dhandle.h

## Purpose
Defines the `Sound2DHandleClass` for managing 2D audio samples in the game's audio system.

## Responsibilities
- Wraps a 2D audio sample handle (`HSAMPLE`).
- Provides methods to control playback (start, stop, resume, etc.).
- Manages sample properties (volume, pan, loop count, playback rate).
- Inherits from `SoundHandleClass` for base functionality.

## Key Types
- **Sound2DHandleClass (Class)**: Handles 2D audio sample playback and properties.

## Key Functions
### `Sound2DHandleClass()`
- Purpose: Default constructor.
- Calls: None.

### `~Sound2DHandleClass()`
- Purpose: Destructor.
- Calls: None.

### `Get_HSAMPLE()`
- Purpose: Returns the underlying `HSAMPLE` handle.
- Calls: None.

### `Set_Miles_Handle(uint32 handle)`
- Purpose: Sets the Miles audio handle.
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
- Calls: None.

### `Get_Sample_Pan()`
- Purpose: Gets the current pan of the sample.
- Calls: None.

### `Set_Sample_Vol
