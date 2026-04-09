# Generals/Code/Libraries/Source/WWVegas/WWAudio/soundstreamhandle.h

## Purpose
Defines the `SoundStreamHandleClass` for managing audio stream handles in the game's sound system.

## Responsibilities
- Wraps Miles Sound System handles for audio streams/samples
- Provides control methods for playback, volume, pan, and position
- Inherits from `SoundHandleClass` for base functionality
- Manages user data and playback rate for audio samples

## Key Types
- **SoundStreamHandleClass (Class)**: Wrapper for audio stream/sample handles with playback control methods.

## Key Functions
### SoundStreamHandleClass()
- Purpose: Default constructor.
- Calls: None.

### ~SoundStreamHandleClass()
- Purpose: Destructor.
- Calls: None.

### As_SoundStreamHandleClass()
- Purpose: RTTI cast to `SoundStreamHandleClass`.
- Calls: None.

### Get_HSAMPLE()
- Purpose: Returns the sample handle.
- Calls: None.

### Get_HSTREAM()
- Purpose: Returns the stream handle.
- Calls: None.

### Set_Miles_Handle()
- Purpose: Sets the Miles Sound System handle.
- Calls: None.

### Initialize()
- Purpose: Initializes the sound buffer.
- Calls: None.

### Start_Sample()
- Purpose: Starts sample playback.
- Calls: None.

### Stop_Sample()
- Purpose: Stops sample playback.
- Calls: None.

### Resume_Sample()
- Purpose: Resumes paused sample playback.
- Calls: None.

### End_Sample()
- Purpose: Ends sample playback.
- Calls: None.

### Set_Sample_Pan()
- Purpose: Sets sample pan (stereo position).
- Calls: None.

### Get_Sample_Pan()
- Purpose: Gets current sample pan.
- Calls: None
