# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundScene.cpp

## Purpose
Manages the audio scene, including sound culling, listener updates, and sound collection for spatial audio in the game.

## Responsibilities
- Manages dynamic and static sound culling systems
- Handles logical sound collection and notification
- Updates listener positions and processes audible sounds
- Supports save/load functionality for sound scenes
- Manages sound scene partitioning and flushing

## Key Types
- SoundSceneClass (Class): Main audio scene manager
- AudibleInfoClass (Class): Stores audible sound information
- (anonymous enum) (Enum): Chunk IDs for save/load
- CHUNKID_VARIABLES (Enum): Variable chunk ID
- CHUNKID_STATIC_SOUNDS (Enum): Static sounds chunk ID
- CHUNKID_DYNAMIC_SOUNDS (Enum): Dynamic sounds chunk ID
- VARID_MIN_DIM (Enum): Minimum dimension variable ID
- VARID_MAX_DIM (Enum): Maximum dimension variable ID

## Key Functions
### Collect_Logical_Sounds
- Purpose: Collects and processes logical sounds for listeners
- Calls: GetTickCount, LogicalListenerClass methods, SoundCullObjClass methods

### Collect_Audible_Sounds
- Purpose: Collects audible dynamic and static sounds for a listener
- Calls: Listener3DClass methods, SoundCullObjClass methods

### On_Frame_Update
- Purpose: Updates the sound scene each frame
- Calls: Listener3DClass methods, Collect_Audible_Sounds, AudibleSoundClass methods

### Save_Static
- Purpose: Saves static scene data
- Calls: ChunkSaveClass methods, Save_Static_Sounds

### Load_Static
- Purpose: Loads static scene data
- Calls: ChunkLoadClass methods, Load_Static_Sounds

## Globals
- MAX_LOGICAL_LISTENER_UPDATES_PER_FRAME (int): Maximum listener updates per frame

## Dependencies
- soundscene.h, soundcullobj.h, logicalsound.h, logicallistener.h, chunkio.h, persistfactory.h, wwprofile.h, threads.h, wwmemlog.h
- Listener3DClass, LogicalListenerClass, AudibleSoundClass, SoundCullObjClass, ChunkSaveClass, ChunkLoadClass, PersistFactoryClass, SaveLoadSystemClass
