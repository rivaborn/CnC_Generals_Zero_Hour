# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundScene.h

## Purpose
Defines the `SoundSceneClass` for spatial audio management in the SAGE engine, handling sound culling and listener positioning.

## Responsibilities
- Manages dynamic and static sound objects in a 3D scene
- Handles logical sounds and listeners for game events
- Performs spatial culling to optimize audio processing
- Supports scene partitioning and save/load functionality

## Key Types
- **SoundSceneClass (Class)**: Main audio scene manager
- **AudibleInfoClass (Class)**: Helper struct for sound distance tracking
- **DynamicSoundCullClass (Class)**: Grid-based culling for dynamic sounds
- **StaticSoundCullClass (Class)**: AABB tree culling for static sounds
- **Listener3DClass (Forward)**: Audio listener interface

## Key Functions
### SoundSceneClass()
- Purpose: Constructor initializes audio scene
- Calls: `Initialize()`

### Add_Sound()
- Purpose: Adds a dynamic audible sound to the scene
- Calls: `Update_Sound()`

### Add_Static_Sound()
- Purpose: Adds a static sound that won't move
- Calls: `Update_Sound()`

### Collect_Audible_Sounds()
- Purpose: Gathers sounds audible to a listener
- Calls: Culling system methods

### On_Frame_Update()
- Purpose: Updates audio scene per frame
- Calls: `Collect_Logical_Sounds()`, culling system updates

## Globals
- **m_Listener (Listener3DClass*)**: Primary audio listener
- **m_2ndListener (Listener3DClass*)**: Secondary listener
- **m_IsBatchMode (bool)**: Batch processing flag

## Dependencies
- `aabtreecull.h`, `gridcull.h`, `listener.h`, `vector.h`
- `soundcullobj.h`, `logicallistener.h`, `multilist.h`
- `RenderObjClass`, `ChunkSaveClass`, `ChunkLoadClass` (forward declarations)
