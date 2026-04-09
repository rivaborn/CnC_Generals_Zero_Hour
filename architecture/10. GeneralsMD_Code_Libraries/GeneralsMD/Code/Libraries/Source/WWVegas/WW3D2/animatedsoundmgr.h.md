# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/animatedsoundmgr.h

## Purpose
Manages animated sound playback for 3D animations in the game engine.

## Responsibilities
- Initializes and shuts down sound management system
- Retrieves embedded sound names from animations
- Triggers sounds during animation frame transitions
- Bridges sound library with WW3D animation system

## Key Types
- **AnimatedSoundMgrClass (Class)**: Main sound manager for animations
- **AnimSoundInfo (Struct)**: Stores sound info (frame, name, 2D flag, stop flag)
- **AnimSoundList (Struct)**: Container for sound info list and bone name
- **ANIM_SOUND_INFO (Typedef)**: Alias for AnimSoundInfo
- **ANIM_SOUND_LIST (Typedef)**: Alias for AnimSoundList

## Key Functions
### Initialize
- Purpose: Initializes the sound manager with optional INI file
- Calls: Not inferable

### Shutdown
- Purpose: Cleans up sound manager resources
- Calls: Not inferable

### Trigger_Sound
- Purpose: Plays sound during animation frame transition
- Calls: Not inferable

### Find_Sound_List
- Purpose: Locates sound list for a given animation
- Calls: Not inferable

## Globals
- **AnimationNameHash (HashTemplateClass)**: Maps animation names to sound lists
- **AnimSoundLists (DynamicVectorClass)**: Stores active sound lists
- **SoundLibrary (SoundLibraryBridgeClass**)**: Pointer to sound library bridge

## Dependencies
- "simplevec.h", "vector.h", "hashtemplate.h"
- HTreeClass, HAnimClass, Matrix3D, SoundLibraryBridgeClass (forward declarations)
