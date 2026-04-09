# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/WWAudio.cpp

## Purpose
Manages audio playback, sound caching, and device initialization for the SAGE engine.

## Responsibilities
- Initializes and manages 2D/3D audio devices using Miles Sound System (MSS)
- Handles sound buffer caching and retrieval
- Manages logical sound types and listeners
- Loads/saves audio settings from registry
- Provides file I/O callbacks for MSS

## Key Types
- WWAudioClass (Class): Main audio manager singleton
- SoundBufferClass (Class): Represents loaded sound data
- LogicalSoundClass (Class): Logical sound type container
- LogicalListenerClass (Class): Listener position manager
- CACHE_ENTRY_STRUCT (Struct): Sound cache entry metadata

## Key Functions
### Open_2D_Device
- Purpose: Initializes 2D audio playback device
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
- MSS API (AIL_* functions)
- Windows API (waveOut, registry)
- WWLib utilities (FileClass, RegistryClass)
- Audio-specific classes (SoundBufferClass, SoundSceneClass)
- Memory management (W3DNEW, REF_PTR_RELEASE)
