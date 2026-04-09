# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AudibleSound.cpp

## Purpose
Implements the AudibleSoundClass and AudibleSoundDefinitionClass for sound management in the WWAudio system.

## Responsibilities
- Manages sound playback, state, and properties (volume, pan, priority, etc.)
- Handles 2D and 3D sound instances with spatial properties
- Serializes/deserializes sound objects for save/load
- Integrates with logical sound system for spatial audio cues
- Manages Miles audio handles and sound buffers

## Key Types
- **AudibleSoundClass (Class)**: Core sound object with playback state and properties
- **AudibleSoundDefinitionClass (Class)**: Sound definition with default settings and creation logic
- **VARID_* (Enums)**: Chunk IDs for save/load serialization
- **CHUNKID_* (Enums)**: Chunk identifiers for save/load

## Key Functions
### Play
- Purpose: Starts sound playback and initializes associated logical sound
- Calls: WWAudioClass::Add_To_Playlist, m_SoundHandle->Start_Sample, On_Event, m_LogicalSound->Add_To_Scene

### Save/Load
- Purpose: Serializes/deserializes sound state and properties
- Calls: ChunkSaveClass/ChunkLoadClass methods, SoundSceneObjClass::Save/Load

### Create_Sound
- Purpose: Factory method to create sound instances from definitions
- Calls: WWAudioClass::Create_3D_Sound, WWAudioClass::Create_Sound_Effect

## Globals
- **_SoundDefFactory (SimpleDefinitionFactoryClass)**: Factory for sound definitions
- **_AudibleSoundDefPersistFactory (SimplePersistFactoryClass)**: Persistence factory for definitions
- **_AudibleSoundPersistFactory (SimplePersistFactoryClass)**: Persistence factory for sound instances

## Dependencies
- **Headers**: audiblesound.h, wwaudio.h, ww3d.h, soundbuffer.h, soundscene.h, logicalsound.h
- **External**: Miles Sound System (via WWAudio), W3D math library, ChunkSave/Load classes
