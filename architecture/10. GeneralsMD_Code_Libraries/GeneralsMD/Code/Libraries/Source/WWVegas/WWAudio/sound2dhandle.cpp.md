# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/sound2dhandle.cpp

## Purpose
Implements the Sound2DHandleClass for managing 2D audio samples using the MILES audio library.

## Responsibilities
- Wraps MILES audio sample operations for 2D sound
- Manages sample playback, volume, pan, and loop settings
- Handles sample position and playback rate control
- Provides user data attachment to samples

## Key Types
- **Sound2DHandleClass (Class)**: Manages 2D audio sample playback and properties
- **SoundBufferClass (Class)**: Used for sound data (external)

## Key Functions
### Initialize
- Purpose: Initializes the sample handle and loads sound data
- Calls: `AIL_init_sample`, `AIL_set_named_sample_file`

### Start_Sample
- Purpose: Starts playback of the audio sample
- Calls: `AIL_start_sample`

### Stop_Sample
- Purpose: Stops playback of the audio sample
- Calls: `AIL_stop_sample`

### Set_Sample_Volume
- Purpose: Sets the volume of the audio sample
- Calls: `AIL_set_sample_volume`

### Get_Sample_Volume
- Purpose: Retrieves the current volume of the audio sample
- Calls: `AIL_sample_volume`

### Set_Sample_Pan
- Purpose: Sets the pan (left/right balance) of the audio sample
- Calls: `AIL_set_sample_pan`

### Set_Sample_Loop_Count
- Purpose: Sets the number of times the sample should loop
- Calls: `AIL_set_sample_loop_count`

### Set_Sample_Playback_Rate
- Purpose: Sets the playback rate (speed) of the sample
- Calls: `AIL_set_sample_playback_rate`

## Globals
- None

## Dependencies
- `sound2dhandle.h` (header)
- `audiblesound.h` (header)
- MILES audio library functions (`AIL_*`)
