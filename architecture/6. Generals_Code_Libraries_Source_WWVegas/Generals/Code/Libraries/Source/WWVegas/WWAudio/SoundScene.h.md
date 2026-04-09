# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundScene.h

## Purpose
Manages spatial audio culling and sound scene management for 3D audio in the game engine.

## Responsibilities
- Manages dynamic and static sound objects in a 3D space
- Handles listener positioning and audio culling
- Supports logical sounds and listeners for scripted audio
- Provides save/load functionality for sound scenes
- Efficiently collects audible sounds for playback

## Key Types
- **SoundSceneClass (Class)**: Main sound scene manager
- **AudibleInfoClass (Class)**: Helper class for tracking audible sounds
- **DynamicSoundCullClass (Class)**: Grid-based culling system for dynamic sounds
- **StaticSoundCullClass (Class)**: AABB tree culling system for static sounds
- **Listener3DClass (Forward reference)**: Audio listener implementation

## Key Functions
### SoundSceneClass::Add_Sound
- Purpose: Adds a dynamic audible sound to the scene
- Calls: Not inferable

### SoundSceneClass::Add_Static_Sound
- Purpose: Adds a static audible sound to the scene
- Calls: Not inferable

### SoundSceneClass::Collect_Audible_Sounds
- Purpose: Collects sounds audible to a specific listener
- Calls: Not inferable

### SoundSceneClass::On_Frame_Update
- Purpose: Updates sound scene state each frame
- Calls: Not inferable

## Globals
- None

## Dependencies
- "aabtreecull.h", "gridcull.h", "listener.h", "vector.h", "priorityvector.h", "soundcullobj.h", "logicallistener.h", "multilist.h"
- RenderObjClass, ChunkSaveClass, ChunkLoadClass (forward declarations)
- AudibleSoundClass, LogicalSoundClass, LogicalListenerClass (assumed from context)
