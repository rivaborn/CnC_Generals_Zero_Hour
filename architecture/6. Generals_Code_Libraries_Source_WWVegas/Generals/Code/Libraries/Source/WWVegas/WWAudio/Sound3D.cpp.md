# Generals/Code/Libraries/Source/WWVegas/WWAudio/Sound3D.cpp

## Purpose
Manages 3D positional audio in the game using the Miles Sound System (MSS).

## Responsibilities
- Handles 3D sound positioning, velocity, and orientation
- Manages sound scene integration and culling
- Implements auto-calculation of sound velocity
- Provides persistence via chunk saving/loading
- Interfaces with the Miles audio system

## Key Types
- Sound3DClass (Class): Core 3D sound management
- (anonymous enum) (Enum): Chunk ID definitions
- CHUNKID_VARIABLES (Enum): Variable chunk ID
- CHUNKID_BASE_CLASS (Enum): Base class chunk ID
- (anonymous enum) (Enum): Variable IDs for persistence
- VARID_AUTO_CALC_VEL (Enum): Auto-calc velocity flag ID
- VARID_CURR_VEL (Enum): Current velocity ID
- VARID_XXX1 (Enum): Unused variable ID
- VARID_XXX2 (Enum): Unused variable ID
- VARID_MAX_VOL_RADIUS (Enum): Max volume radius ID
- VARID_IS_STATIC (Enum): Static sound flag ID

## Key Functions
### Play
- Purpose: Starts sound playback and records initial tick time
- Calls: AudibleSoundClass::Play

### On_Frame_Update
- Purpose: Updates sound position and velocity each frame
- Calls: m_Scene->Update_Sound, Apply_Auto_Position, AudibleSoundClass::On_Frame_Update

### Set_Transform
- Purpose: Updates sound's world transformation matrix
- Calls: Set_Dirty, Update_Miles_Transform

### Update_Miles_Transform
- Purpose: Converts sound position to listener space and updates Miles
- Calls: ::AIL_set_3D_position, ::AIL_set_3D_orientation

### Set_Velocity
- Purpose: Sets sound's velocity vector
- Calls: ::AIL_set_3D_velocity_vector

### Initialize_Miles_Handle
- Purpose: Configures Miles sound handle with current settings
- Calls: m_SoundHandle->Initialize, m_SoundHandle->Get_Sample_MS_Position, m_SoundHandle->Set_Sample_Volume, m_SoundHandle->Set_Sample_Pan, m_SoundHandle->Set_Sample_Loop_Count, ::AIL_set_3D_sample_distances, ::AIL_set_3D_sample_effects_level, Update_Miles_Transform, m_SoundHandle->Start_Sample, m_SoundHandle->Set_Sample_Loop_Count, Seek, m_SoundHandle->Set_Sample_User_Data

### Save/Load
- Purpose: Persistence via chunk system
- Calls: AudibleSoundClass::Save/Load, WRITE_MICRO_CHUNK/READ_MICRO_CHUNK

## Globals
- _Sound3DPersistFactory (SimplePersistFactoryClass<Sound3DClass, CHUNKID_SOUND3D>): Persistence factory for Sound3DClass

## Dependencies
- sound3d.h, soundbuffer.h, wwaudio.h, soundscene.h, utils.h, soundchunkids.h, persistfactory.h, chunkio.h, sound3dhandle.h
- MMSLockClass, Vector3, Matrix3D, AIL functions (::AIL_set_3D_position, ::AIL_set_3D_orientation, ::AIL_set_3D_velocity_vector, ::AIL_set_3D_sample_distances, ::AIL_set_3D_sample_effects_level)
- WWA
