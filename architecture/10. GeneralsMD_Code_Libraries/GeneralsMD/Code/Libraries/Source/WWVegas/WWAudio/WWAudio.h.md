# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/WWAudio.h

## Purpose
Header file defining the WWAudioClass, the main audio controller for music and sound effects in the game.

## Responsibilities
- Manages 2D and 3D audio drivers
- Handles sound caching and playback
- Controls volume and playback settings
- Manages sound scenes and logical sound types

## Key Types
- WWAudioClass (Class): Main audio controller
- AudibleSoundClass (Class): Base sound object
- Sound3DClass (Class): 3D sound object
- SoundSceneClass (Class): 3D sound scene manager
- SOUND_CLASSID (Enum): Sound object class IDs
- DRIVER_TYPE_2D/DRIVER_TYPE_3D (Enum): Audio driver types
- CACHE_ENTRY_STRUCT (Struct): Sound cache entry
- LOGICAL_TYPE_STRUCT (Struct): Logical sound type

## Key Functions
### Initialize
- Purpose: Initializes audio system with specified settings
- Calls: Open_2D_Device, Build_3D_Driver_List, Select_3D_Device

### Create_Sound_Effect
- Purpose: Creates a 2D sound effect
- Calls: Get_Sound_Buffer, Is_OK_To_Give_Handle

### Create_3D_Sound
- Purpose: Creates a 3D sound effect
- Calls: Get_Sound_Buffer, Validate_3D_Sound_Buffer

### On_Frame_Update
- Purpose: Updates audio system state
- Calls: Reprioritize_Playlist, Free_Cache_Space

### Simple_Play_2D_Sound_Effect
- Purpose: Plays a simple 2D sound effect
- Calls: Create_Sound_Effect, Add_To_Playlist

## Globals
- DEF_2D_SAMPLE_COUNT (int): Default 2D sample count
- DEF_3D_SAMPLE_COUNT (int): Default 3D sample count
- DEF_MUSIC_VOL (float): Default music volume
- DEF_SFX_VOL (float): Default sound effects volume
- DEF_CACHE_SIZE (int): Default cache size
- DEF_MAX_2D_BUFFER_SIZE (int): Default max 2D buffer size
- DEF_MAX_3D_BUFFER_SIZE (int): Default max 3D buffer size

## Dependencies
- Mss.H (Miles Sound System)
- Vector.H (dynamic vector)
- SoundBuffer.H (sound buffer)
- AudioEvents.H (audio callbacks)
- wwstring.h (string handling)
