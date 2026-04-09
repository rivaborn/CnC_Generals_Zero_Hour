# Generals/Code/Libraries/Source/WWVegas/WWAudio/WWAudio.cpp

## Purpose
Manages audio playback, sound caching, and device initialization for the game using the Miles Sound System (MSS).

## Responsibilities
- Initializes and manages 2D/3D audio devices
- Handles sound buffer caching and retrieval
- Manages logical sound types and listeners
- Interfaces with registry for audio settings
- Provides callbacks for file I/O operations

## Key Types
- WWAudioClass (Class): Main audio manager singleton
- SoundBufferClass (Class): Represents loaded sound data
- LogicalSoundClass (Class): Abstract sound type
- LogicalListenerClass (Class): Audio listener interface
- CACHE_ENTRY_STRUCT (Struct): Sound cache entry metadata

## Key Functions
### Open_2D_Device
- Purpose: Initializes the 2D audio playback device
- Calls: AIL_waveOutOpen, AIL_set_preference, Allocate_2D_Handles

### Get_Sound_Buffer
- Purpose: Retrieves or creates a sound buffer from cache or file
- Calls: Find_Cached_Buffer, Get_File, Create_Sound_Buffer

### Load_From_Registry
- Purpose: Loads audio settings from Windows registry
- Calls: RegistryClass methods, Open_2D_Device, Build_3D_Driver_List

### File_Open_Callback
- Purpose: MSS callback for opening sound files
- Calls: Get_File

## Globals
- VALUE_NAME_IS_STEREO (const char*): Registry key for stereo setting
- VALUE_NAME_BITS (const char*): Registry key for audio bit depth
- VALUE_NAME_HERTZ (const char*): Registry key for sample rate
- _theInstance (WWAudioClass*): Singleton instance pointer
- _TimerSyncEvent (HANDLE): Synchronization event handle

## Dependencies
- Windows.h, WWAudio.h, WWDebug.h, SoundBuffer.h, AudibleSound.h
- AIL (Miles Sound System) API functions
- Registry.h for configuration storage
- FileClass for audio file handling
