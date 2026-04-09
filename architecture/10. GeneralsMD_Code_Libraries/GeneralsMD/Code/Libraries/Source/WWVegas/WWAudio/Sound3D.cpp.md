# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/Sound3D.cpp

## Purpose
Manages 3D positional audio in the game using the Miles Sound System (MSS).

## Responsibilities
- Handles 3D sound positioning, velocity, and orientation
- Manages sound scene integration and culling
- Implements sound persistence via chunk I/O
- Updates audio parameters per frame
- Interfaces with the Miles audio system

## Key Types
- Sound3DClass (Class): Core 3D sound object with position/velocity tracking
- (anonymous enum) (Enum): Chunk ID constants for serialization
- (anonymous enum) (Enum): Variable ID constants for sound properties

## Key Functions
### Play
- Purpose: Starts sound playback and records initial tick time
- Calls: AudibleSoundClass::Play

### On_Frame_Update
- Purpose: Updates sound position, velocity, and transform per frame
- Calls: Apply_Auto_Position, Set_Velocity, AudibleSoundClass::On_Frame_Update

### Update_Miles_Transform
- Purpose: Synchronizes sound transform with Miles audio system
- Calls: AIL_set_3D_position, AIL_set_3D_orientation

### Set_Velocity
- Purpose: Updates sound velocity and propagates to Miles
- Calls: AIL_set_3D_velocity_vector

### Initialize_Miles_Handle
- Purpose: Configures Miles sound handle with cached parameters
- Calls: AIL_set_3D_sample_distances, AIL_set_3D_sample_effects_level

## Globals
- _Sound3DPersistFactory (SimplePersistFactoryClass): Persistence factory for Sound3DClass

## Dependencies
- sound3d.h, soundbuffer.h, wwaudio.h, soundscene.h, utils.h, soundchunkids.h, persistfactory.h, chunkio.h, sound3dhandle.h
- AIL_* functions from Miles Sound System
- Matrix3D, Vector3 classes
- MMSLockClass for thread safety
