# Generals/Code/Libraries/Source/WWVegas/WWAudio/AudibleSound.cpp

## Purpose
Manages audible sound objects in the game, including 2D/3D sound effects, playback control, and serialization.

## Responsibilities
- Handles sound playback, pausing, stopping, and seeking
- Manages sound buffer loading and Miles audio handle allocation
- Implements save/load functionality for sound state
- Supports 3D spatial audio with transform tracking
- Manages logical sound associations for spatial audio cues

## Key Types
- **AudibleSoundClass** (Class): Core sound object with playback state and properties
- **AudibleSoundDefinitionClass** (Class): Sound definition with configuration parameters
- **VARID_* enums** (Enum): Save/load variable identifiers for serialization

## Key Functions
### Play
- Purpose: Starts sound playback and initializes associated logical sound
- Calls: WWAudioClass::Add_To_Playlist, m_SoundHandle->Start_Sample, On_Event, m_LogicalSound->Add_To_Scene

### Save/Load
- Purpose: Serializes/deserializes sound state and configuration
- Calls: ChunkSaveClass/ChunkLoadClass methods, SoundSceneObjClass::Save/Load

### Create_Sound
- Purpose: Factory method to create sound instances from definitions
- Calls: WWAudioClass::Create_3D_Sound, WWAudioClass::Create_Sound_Effect

## Globals
- **_SoundDefFactory** (DefinitionFactoryClass): Factory for sound definitions
- **_AudibleSoundDefPersistFactory** (SimplePersistFactoryClass): Persistence factory for definitions
- **_AudibleSoundPersistFactory** (SimplePersistFactoryClass): Persistence factory for sound instances

## Dependencies
- audiblesound.h, wwaudio.h, ww3d.h, soundbuffer.h, soundscene.h
- threads.h, soundchunkids.h, persistfactory.h, logicalsound.h
- Miles SDK (via SoundStreamHandle/Sound2DHandle)
