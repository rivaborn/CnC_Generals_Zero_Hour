# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/animatedsoundmgr.cpp

## Purpose
Manages animated sound effects for 3D animations in the game engine, loading sound definitions from INI files and triggering sounds at specific animation frames.

## Responsibilities
- Loads and parses sound definitions from INI files
- Manages sound lists associated with animations
- Triggers sounds at specific animation frames
- Handles 2D/3D sound playback and sound stopping

## Key Types
- **AnimatedSoundMgrClass**: Main manager class for animated sounds
- **ANIM_SOUND_LIST (struct)**: Contains sound info list and bone name
- **ANIM_SOUND_INFO (struct)**: Stores frame, sound name, and playback flags
- **SoundLibraryBridgeClass**: Interface for sound playback (external)

## Key Functions
### Get_INI
- Purpose: Loads an INI file from the file factory
- Calls: _TheFileFactory->Get_File, _TheFileFactory->Return_File

### Build_List_From_String
- Purpose: Parses a comma-delimited string into an array of StringClass objects
- Calls: strlen, strstr, strnicmp, new

### Is_In_Param_List
- Purpose: Checks if a parameter exists in a parameter list
- Calls: strstr

### Initialize
- Purpose: Initializes the sound manager and loads sound definitions
- Calls: Get_INI, AnimationNameHash.Insert, AnimSoundLists.Add

### Trigger_Sound
- Purpose: Triggers sounds when animation crosses specific frames
- Calls: Find_Sound_List, SoundLibrary->Play_2D_Audio, SoundLibrary->Play_3D_Audio, SoundLibrary->Stop_Playing_Audio

## Globals
- **AnimationNameHash (HashTemplateClass)**: Maps animation names to sound lists
- **AnimSoundLists (DynamicVectorClass)**: Stores all sound lists
- **SoundLibrary (SoundLibraryBridgeClass**)**: Pointer to sound playback interface

## Dependencies
- Key includes: animatedsoundmgr.h, ini.h, inisup.h, ffactory.h, wwaudio.h, audiblesound.h, htree.h, hanim.h, soundlibrarybridge.h
- External symbols: _TheFileFactory, WWDEBUG_SAY, WWMath::Fabs
