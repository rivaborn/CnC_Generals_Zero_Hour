# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_emt.cpp

## Purpose
Manages particle emitters in the game's 3D rendering system, handling emission logic, particle initialization, and scene integration.

## Responsibilities
- Creates and manages particle emitters with configurable properties (velocity, color, size, etc.)
- Handles particle emission timing and burst logic
- Integrates with the scene system for rendering and updates
- Supports serialization and cloning of emitter definitions

## Key Types
- **ParticleEmitterClass (Class)**: Main emitter class managing particle generation and behavior
- **ParticleEmitterDefClass (Class)**: Definition structure for saving/loading emitter properties
- **Vector3Randomizer (Class)**: Handles random position/velocity variations
- **ParticlePropertyStruct (Struct)**: Template struct for animated properties (color, opacity, etc.)

## Key Functions
### Create_From_Definition
- Purpose: Creates a particle emitter from a definition structure
- Calls: WW3DAssetManager::Get_Instance(), TextureClass methods, ParticleBufferClass constructor

### Emit
- Purpose: Emits particles based on current frame time and emitter settings
- Calls: Create_New_Particles, WW3D::Get_Frame_Time, Quaternion/Slerp functions

### Initialize_Particle
- Purpose: Initializes a new particle's position, velocity, and properties
- Calls: Vector3Randomizer::Get_Vector, Quaternion::Rotate_Vector

### Build_Definition
- Purpose: Creates a definition object from current emitter state
- Calls: ParticleEmitterDefClass methods, various getter functions

## Globals
- **InheritedWorldSpaceEmitterVel (Vector3)**: Stores emitter velocity for particle inheritance
- **DebugDisable (bool)**: Global flag to disable particle generation
- **DefaultRemoveOnComplete (bool)**: Controls whether emitters are removed after completion

## Dependencies
- Key includes: "part_emt.h", "ww3d.h", "assetmgr.h", "part_ldr.h", "scene.h"
- External symbols: WW3DAssetManager, SceneClass, TextureClass, ShaderClass
- WW3D engine systems: Rendering, scene management, asset loading
