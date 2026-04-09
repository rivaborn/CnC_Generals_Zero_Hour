# Generals/Code/Libraries/Source/WWVegas/WWAudio/WWAudio.h

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
- DRIVER_TYPE_2D/DRIVER_TYPE_3D (Enums): Audio driver types

## Key Functions
### Initialize
- Purpose: Initializes audio system with specified settings
- Calls: Open_2D_Device, Select_3D_Device

### Create_Sound_Effect
- Purpose: Creates a 2D sound effect from file or memory
- Calls: Get_Sound_Buffer, Cache_Buffer

### Create_3D_Sound
- Purpose: Creates a 3D sound effect from file or memory
- Calls: Get_Sound_Buffer, Cache_Buffer

### On_Frame_Update
- Purpose: Updates audio system state
- Calls: Reprioritize_Playlist, Free_Completed_Sounds

## Globals
- DEF_2D_SAMPLE_COUNT (int): Default 2D sample count
- DEF_3D_SAMPLE_COUNT (int): Default 3D sample count
- DEF_MUSIC_VOL (float): Default music volume
- DEF_SFX_VOL (float): Default sound effects volume
- DEF_CACHE_SIZE (int): Default cache size in KB

## Dependencies
- Mss.H (Miles Sound System)
- Vector.H (dynamic arrays)
- SoundBuffer.H (sound buffer management)
- AudioEvents.H (audio callbacks)
- wwstring.h (string handling)
