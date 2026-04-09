# Generals/Code/Libraries/Source/WWVegas/WWAudio/soundstreamhandle.cpp

## Purpose
Manages audio stream handles using the MILES sound system for the game's audio subsystem.

## Responsibilities
- Wraps MILES stream operations (play, pause, stop, volume, pan, etc.)
- Handles stream initialization and cleanup
- Provides access to stream properties (position, loop count, playback rate)
- Manages user data associated with streams

## Key Types
- **SoundStreamHandleClass (Class)**: Manages audio stream handles and their properties.

## Key Functions
### Initialize
- Purpose: Sets up the stream handle from a sound buffer.
- Calls: `SoundHandleClass::Initialize`, `AIL_open_stream_by_sample`

### Start_Sample
- Purpose: Starts playback of the audio stream.
- Calls: `AIL_start_stream`

### Stop_Sample
- Purpose: Pauses the audio stream.
- Calls: `AIL_pause_stream`

### Resume_Sample
- Purpose: Resumes playback of a paused stream.
- Calls: `AIL_pause_stream`

### End_Sample
- Purpose: Stops and releases the stream handle.
- Calls: `Stop_Sample`, `AIL_close_stream`

### Set_Sample_Pan
- Purpose: Adjusts the stereo pan of the stream.
- Calls: `AIL_set_stream_pan`

### Get_Sample_Pan
- Purpose: Retrieves the current pan setting.
- Calls: `AIL_stream_pan`

### Set_Sample_Volume
- Purpose: Sets the stream's volume level.
- Calls: `AIL_set_stream_volume`

### Get_Sample_Volume
- Purpose: Gets the current volume level.
- Calls: `AIL_stream_volume`

### Set_Sample_Loop_Count
- Purpose: Configures how many times the stream loops.
- Calls: `AIL_set_stream_loop_block`, `AIL_set_stream_loop_count`

### Get_Sample_Loop_Count
- Purpose: Retrieves the current loop count.
- Calls: `AIL_stream_loop_count`

### Set_Sample_MS_Position
- Purpose: Seeks to a specific millisecond position in the stream.
- Calls: `AIL_set_stream_ms_position`

### Get_Sample_MS_Position
- Purpose: Gets the current playback position and length.
- Calls: `AIL_stream_ms_position`

### Set_Sample_User_Data
- Purpose: Associates user data with the sample handle.
- Calls: `AIL_set_sample_user_data`

### Get_Sample_User_Data
- Purpose: Retrieves user data from the sample handle.
- Calls: `AIL_sample_user_data`

### Get_Sample_Playback_Rate
- Purpose:
