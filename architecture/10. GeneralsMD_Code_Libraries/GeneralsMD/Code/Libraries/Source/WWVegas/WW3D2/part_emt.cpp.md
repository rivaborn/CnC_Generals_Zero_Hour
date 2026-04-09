# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_emt.cpp

## Purpose
Manages particle emitters in the game's 3D rendering system, controlling particle creation, behavior, and rendering.

## Responsibilities
- Creates and initializes particle emitters from definitions
- Manages particle emission timing and behavior
- Handles particle velocity inheritance and transformation
- Controls emitter lifecycle (start/stop/restart)
- Serializes emitter definitions for saving/loading

## Key Types
- **ParticleEmitterClass (Class)**: Main particle emitter implementation
- **ParticleEmitterDefClass (Class)**: Definition structure for emitter properties
- **Vector3Randomizer (Class)**: Handles random position/velocity generation
- **NewParticleStruct (Struct)**: Stores particle state data
- **ParticlePropertyStruct (Template)**: Keyframe-based property animation

## Key Functions
### Create_From_Definition
- Purpose: Creates a particle emitter from a definition object
- Calls: WW3DAssetManager::Get_Instance(), TextureClass methods, ParticleBufferClass constructor

### Create_New_Particles
- Purpose: Generates new particles based on emitter parameters
- Calls: Initialize_Particle, WW3D::Get_Frame_Time, Quaternion/Slerp math functions

### Initialize_Particle
- Purpose: Sets up initial state for a new particle
- Calls: Vector3Randomizer::Get_Vector, Quaternion::Rotate_Vector

### On_Frame_Update
- Purpose: Handles per-frame emitter updates and particle emission
- Calls: Buffer->Add, SceneClass registration methods

## Globals
- **InheritedWorldSpaceEmitterVel (Vector3)**: Passes emitter velocity to particle initialization
- **DebugDisable (bool)**: Global flag to disable particle generation
- **DefaultRemoveOnComplete (bool)**: Controls whether emitters auto-remove when done

## Dependencies
- Key includes: part_ldr.h, ww3d.h, assetmgr.h, scene.h, texture.h
- External symbols: WW3DAssetManager, SceneClass, TextureClass, ShaderClass
- Math utilities: Quaternion, Vector3, WWMath functions
