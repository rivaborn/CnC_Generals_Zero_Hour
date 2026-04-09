# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundScene.cpp

## Purpose
Manages the audio scene, including sound culling, listener updates, and sound collection for spatial audio in the game.

## Responsibilities
- Manages dynamic and static sound culling systems
- Handles logical sound collection and notification
- Manages listener positions and updates
- Supports save/load functionality for audio scene state
- Flushes and updates sounds in the scene

## Key Types
- SoundSceneClass (Class): Main audio scene manager
- AudibleInfoClass (Class): Stores audible sound information
- (anonymous enum) (Enum): Chunk IDs for save/load
- CHUNKID_VARIABLES (Enum): Variable chunk ID
- CHUNKID_STATIC_SOUNDS (Enum): Static sounds chunk ID
- CHUNKID_DYNAMIC_SOUNDS (Enum): Dynamic sounds chunk ID
- VARID_MIN_DIM (Enum): Min dimension variable ID
- VARID_MAX_DIM (Enum): Max dimension variable ID

## Key Functions
### Collect_Logical_Sounds
- Purpose: Collects and processes logical sounds for listeners
- Calls: WWPROFILE, GetTickCount, priority_queue.Process_Head, listener->On_Frame_Update, m_LogicalCullingSystem.Collect_Objects, cull_obj->Peek_Sound_Obj, sound_obj->Allow_Notify, listener->On_Event

### Collect_Audible_Sounds
- Purpose: Collects audible dynamic and static sounds for a listener
- Calls: WWPROFILE, listener->Get_Position, m_DynamicCullingSystem.Collect_Objects, m_StaticCullingSystem.Collect_Objects, cull_obj->Peek_Sound_Obj, sound_obj->Get_Position, sound_obj->Get_DropOff_Radius, sound_obj->Set_Runtime_Priority

### On_Frame_Update
- Purpose: Updates the audio scene each frame, including listener and sound updates
- Calls: WWPROFILE, m_2ndListener->On_Frame_Update, Collect_Audible_Sounds, m_Listener->On_Frame_Update, auxiliary_sounds.Remove, primary_sounds.Remove, audible_sounds.Add, sound_obj->On_Added_To_Scene, sound_obj->On_Removed_From_Scene

### Save_Static
- Purpose: Saves static scene data to a chunk
- Calls: csave.Begin_Chunk, WRITE_MICRO_CHUNK, Save_Static_Sounds, csave.End_Chunk

### Load_Static
- Purpose: Loads static scene data from a chunk
- Calls: cload.Open_Chunk, Load_Static_Sounds, cload.Open_Micro_Chunk, READ_MICRO_CHUNK, cload.Close_Micro_Chunk, cload.Close_Chunk, Re_Partition, On_Frame_Update

## Globals
- MAX_LOGICAL_LISTENER_UPDATES_PER_FRAME (int): Maximum listener updates per frame

## Dependencies
- soundscene.h, soundcullobj.h, logicalsound.h, logicallistener.h, chunkio.h, persistfactory.h, wwprofile.h, threads.h, wwmemlog.h
- Listener3DClass, LogicalListenerClass, LogicalSoundClass, AudibleSoundClass, SoundCullObjClass, ChunkSaveClass, ChunkLoadClass, PersistFactoryClass, SaveLoadSystemClass, WWAudioThreadsClass
