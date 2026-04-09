# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_buf.h

## Purpose
Defines the `ParticleBufferClass` and related structures for particle system rendering in the SAGE engine.

## Responsibilities
- Manages particle state (position, velocity, color, size, etc.)
- Handles particle rendering (points, lines, line groups)
- Implements LOD (Level of Detail) for performance optimization
- Synchronizes with `ParticleEmitterClass` for new particle generation
- Maintains bounding volumes and collision detection

## Key Types
- **ParticleBufferClass (Class)**: Core particle system renderer.
- **NewParticleStruct (Struct)**: Data structure for new particles emitted by the emitter.
- **TailDiffuseTypeEnum (Enum)**: Defines tail color modes for line rendering (BLACK, WHITE, SAME_AS_HEAD, SAME_AS_HEAD_ALPHA_ZERO).

## Key Functions
### `Render(RenderInfoClass & rinfo)`
- Purpose: Renders the particle system based on current state.
- Calls: `Render_Particles`, `Render_Line`, `Render_Line_Group`, `Update_Kinematic_Particle_State`, `Update_Visual_Particle_State`.

### `Update_Kinematic_Particle_State()`
- Purpose: Updates particle positions, velocities, and lifetimes.
- Calls: `Get_New_Particles`, `Kill_Old_Particles`, `Update_Non_New_Particles`.

### `Generate_APT(ShareBufferClass<unsigned int> **apt, unsigned int &active_point_count)`
- Purpose: Generates an active point table for rendering optimization.
- Calls: None (internal helper).

### `Determine_Tail_Diffuse()`
- Purpose: Determines tail color based on shader and texture settings.
- Calls: None (internal logic).

## Globals
- **TotalActiveCount (unsigned int)**: Tracks total active particle buffers.
- **LODMaxScreenSizes[17] (float)**: Static array for LOD screen-size clamps.
- **PermutationArray[16] (unsigned int)**: Random permutation for particle decimation.

## Dependencies
- Key includes: `rendobj.h`, `pointgr.h`, `seglinerenderer.h`, `linegrp.h`.
- External symbols: `RenderObjClass`, `ParticleEmitterClass`, `Vector3`, `TextureClass`, `ShaderClass`.
