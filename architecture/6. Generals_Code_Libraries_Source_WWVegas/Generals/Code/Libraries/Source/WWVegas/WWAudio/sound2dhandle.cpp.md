# Generals/Code/Libraries/Source/WWVegas/WWAudio/sound2dhandle.cpp

## Purpose
Implements the Sound2DHandleClass for managing 2D audio samples using the Miles Sound System (MSS) API.

## Responsibilities
- Wraps MSS sample operations for 2D audio playback
- Manages sample state (playback, volume, pan, loops)
- Handles sample initialization and resource loading
- Provides access to sample properties and playback control

## Key Types
- **Sound2DHandleClass (Class)**: Manages 2D audio sample playback via MSS API
- **SoundBufferClass (Class)**: External class for sound buffer data (referenced but not defined here)

## Key Functions
### Initialize
- Purpose: Initializes the sample handle and loads sound data
- Calls: `AIL_init_sample`, `AIL_set_named_sample_file`, `SoundHandleClass::Initialize`

### Start_Sample
- Purpose: Starts playback of the audio sample
- Calls: `AIL_start_sample`

### Stop_Sample
- Purpose: Stops playback of the audio sample
- Calls: `AIL_stop_sample`

### Set_Sample_Pan
- Purpose: Sets the pan (stereo position) of the sample
- Calls: `AIL_set_sample_pan`

### Set_Sample_Volume
- Purpose: Sets the volume of the sample
- Calls: `AIL_set_sample_volume`

### Set_Sample_Loop_Count
- Purpose: Sets the number of times the sample should loop
- Calls: `AIL_set_sample_loop_count`

### Set_Sample_MS_Position
- Purpose: Sets the playback position in milliseconds
- Calls: `AIL_set_sample_ms_position`

### Set_Miles_Handle
- Purpose: Assigns a MSS sample handle to this object
- Calls: None

## Globals
- None

## Dependencies
- `sound2dhandle.h` (header for this class)
- `audiblesound.h` (external audio definitions)
- MSS API functions (`AIL_*` prefix) for sample manipulation
