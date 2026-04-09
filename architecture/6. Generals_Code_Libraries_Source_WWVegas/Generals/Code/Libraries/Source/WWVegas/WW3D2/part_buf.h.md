# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_buf.h

## Purpose
Defines the `ParticleBufferClass` and related structures for particle system rendering in the SAGE engine.

## Responsibilities
- Manages particle state (position, velocity, age, etc.)
- Handles particle rendering (points/lines) with LOD support
- Maintains circular buffers for new/old particles
- Updates particle properties via keyframes and randomizers
- Synchronizes with `ParticleEmitterClass` for new particle generation

## Key Types
- **ParticleBufferClass (Class)**: Main particle buffer render object.
- **NewParticleStruct (Struct)**: Container for new particle data passed from emitter.
- **ParticleEmitterClass (Class)**: Reference to emitter (forward declared).
- **ParticlePropertyStruct (Struct)**: Template for particle property keyframes (forward declared).

## Key Functions
### `Render_Particles`
- Purpose: Renders particles as points.
- Calls: `PointGroup->Render()`

### `Render_Line`
- Purpose: Renders particle system as a line.
- Calls: `LineRenderer->Render()`

### `Update_Kinematic_Particle_State`
- Purpose: Updates particle positions/velocities and manages particle lifecycle.
- Calls: `Get_New_Particles()`, `Kill_Old_Particles()`, `Update_Non_New_Particles()`

### `Update_Visual_Particle_State`
- Purpose: Updates color/size/opacity for rendering.
- Calls: None visible in header.

### `Add_Uninitialized_New_Particle`
- Purpose: Allocates space in new particle queue for emitter.
- Calls: None.

## Globals
- **TotalActiveCount (unsigned int)**: Static counter of active particle buffers.
- **LODMaxScreenSizes[17] (float)**: Static array for LOD screen size thresholds.
- **PermutationArray[16] (unsigned int)**: Static array for particle decimation.

## Dependencies
- `rendobj.h`, `pointgr.h`, `seglinerenderer.h`
- `Vector3`, `Vector4`, `AABoxClass`, `SphereClass`, `TextureClass`, `ShaderClass`
- `RenderInfoClass`, `CameraClass`, `SceneClass`, `ParticleEmitterClass`
