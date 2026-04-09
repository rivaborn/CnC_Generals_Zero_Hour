# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/soundstreamhandle.cpp

## Purpose
Manages audio stream handles using the MILES sound system for the game's audio subsystem.

## Responsibilities
- Wraps MILES audio stream operations (play, pause, stop, volume, pan, etc.)
- Handles stream initialization and cleanup
- Provides access to stream properties (position, loop count, playback rate)
- Manages user data associated with streams

## Key Types
- **SoundStreamHandleClass (Class)**: Manages audio stream handles and their properties
- **HSAMPLE (Type)**: MILES sample handle type
- **HSTREAM (Type)**: MILES stream handle type

## Key Functions
### Initialize
- Purpose: Sets up the audio stream from a sound buffer
- Calls: `SoundHandleClass::Initialize`, `AIL_open_stream_by_sample`

### Start_Sample
- Purpose: Begins playback of the audio stream
- Calls: `AIL_start_stream`

### Stop_Sample
- Purpose: Pauses the audio stream
- Calls: `AIL_pause_stream`

### Resume_Sample
- Purpose: Resumes playback of a paused stream
- Calls: `AIL_pause_stream`

### End_Sample
- Purpose: Stops and releases the stream handle
- Calls: `Stop_Sample`, `AIL_close_stream`

### Set_Sample_Pan
- Purpose: Adjusts the stereo pan of the stream
- Calls: `AIL_set_stream_pan`

### Set_Sample_Volume
- Purpose: Sets the volume level of the stream
- Calls: `AIL_set_stream_volume`

### Set_Sample_Loop_Count
- Purpose: Configures how many times the stream should loop
- Calls: `AIL_set_stream_loop_block`, `AIL_set_stream_loop_count`

### Set_Sample_MS_Position
- Purpose: Seeks to a specific position in the stream (in milliseconds)
- Calls: `AIL_set_stream_ms_position`

### Set_Sample_User_Data
- Purpose: Associates custom data with the sample
- Calls: `AIL_set_sample_user_data`

### Set_Sample_Playback_Rate
- Purpose: Changes the playback speed of the stream
- Calls: `AIL_set_stream_playback_rate`

## Globals
None

## Dependencies
- `soundstreamhandle.h` (header)
- `audiblesound.h` (header)
- MILES Audio Library functions (`AIL_*` prefix)
- `WWAudioClass` singleton for driver access
