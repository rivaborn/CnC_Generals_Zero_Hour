# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_DSoundDriver.cpp

## Purpose
Implements the DirectSound audio driver for the game's audio system, handling sound playback, channel management, and audio format conversion.

## Responsibilities
- Manages DirectSound device initialization and buffer creation
- Handles audio playback, pausing, stopping, and channel management
- Implements audio format conversion (PCM, IMA ADPCM, MS ADPCM, MP3)
- Provides focus handling for audio when the application gains/loses focus
- Maintains audio channels and their playback state

## Key Types
- `AUD_DRV_CHAN` (Class): Represents an audio channel with playback state and buffer management
- `TRANSFER` (Class): Handles audio data transfer and format conversion state
- `IMA_DATA` (Class): Stores state for IMA ADPCM decoding
- `MS_DATA` (Class): Stores state for MS ADPCM decoding
- `MP3_DATA` (Class): Stores state for MP3 decoding

## Key Functions
### `audioOpen`
- Purpose: Initializes the DirectSound device and primary buffer
- Calls: `DirectSoundCreate`, `AUD_restore_primary`

### `audioOpenChannel`
- Purpose: Creates a new audio channel with associated DirectSound buffer
- Calls: `AUD_create_pcm_buffer`, `AUD_init_buffer`

### `audioStart`
- Purpose: Begins playback on an audio channel
- Calls: `AUD_set_buffer_src`, `AUD_fill_buffer`

### `AUD_service_device`
- Purpose: Services all audio channels, updating playback state
- Calls: `AUD_pcm_service`, `AUD_update_buffer`

### `IMA_decode_block`
- Purpose: Decodes IMA ADPCM audio data
- Calls: `ImaAdpcmDecode`

### `MS_decode_block`
- Purpose: Decodes MS ADPCM audio data
- Calls: `MSAdpcmDecode`

## Globals
- `AUD_sound_object` (LPDIRECTSOUND): DirectSound interface object
- `AUD_primary_buffer` (LPDIRECTSOUNDBUFFER): Primary DirectSound buffer
- `AUD_log_table` (int[101]): Volume conversion lookup table
- `AudioSystemDSD` (AudioSystemMaster*): Exported audio system master interface

## Dependencies
- DirectSound API (`dsound.h`)
- WAudio library headers (`device.h`, `channel.h`, `driver.h`)
- MP3 decoding library (`mss.h`, `mp3dec.h`)
- Windows API (`windows.h`, `mmsystem.h`)
