# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_buf.cpp

## Purpose
Manages particle buffer rendering and lifecycle in the SAGE engine, handling particle properties, LOD, and emitter interactions.

## Responsibilities
- Particle property management (color, opacity, size, rotation, frame)
- Particle buffer updates and rendering
- LOD (Level of Detail) control for particles
- Keyframe animation for particle properties
- Randomization tables for particle variation

## Key Types
- **ParticleBufferClass**: Manages particle buffers, including properties, rendering, and LOD.
- **ParticlePropertyStruct<T>**: Template struct for particle properties (color, opacity, size, rotation, frame).
- **NewParticleStruct**: Struct for new particle data in the queue.
- **ShareBufferClass<T>**: Shared buffer for particle data (position, color, etc.).
- **PointGroupClass**: Handles point-based rendering (triangles/quads).
- **SegLineRendererClass**: Manages line-based particle rendering.

## Key Functions
### `ParticleBufferClass()`
- Purpose: Constructs a particle buffer with emitter, properties, and rendering settings.
- Calls: `Reset_Colors`, `Reset_Opacity`, `Reset_Size`, `Reset_Rotations`, `Reset_Frames`, `Calculate_Cost_Value_Arrays`.

### `Update()`
- Purpose: Updates particle positions, velocities, and properties over time.
- Calls: `WW3D::Get_Sync_Time()`, `Get_Projected_Area()`, `Calculate_Cost_Value_Arrays`.

### `Get_Color_Key_Frames()`
- Purpose: Retrieves color keyframes for particle animation.
- Calls: None (directly).

### `Get_Opacity_Key_Frames()`
- Purpose: Retrieves opacity keyframes for particle animation.
- Calls: None (directly).

### `Get_Size_Key_Frames()`
- Purpose: Retrieves size keyframes for particle animation.
- Calls: None (directly).

### `Get_Rotation_Key_Frames()`
- Purpose: Retrieves rotation keyframes for particle animation.
- Calls: None (directly).

### `Get_Frame_Key_Frames()`
- Purpose: Retrieves frame keyframes for particle animation.
- Calls: None (directly).

### `Set_LOD_Max_Screen_Size()`
- Purpose: Sets the maximum screen size for a specific LOD level.
- Calls: None (directly).

### `Get_LOD_Max_Screen_Size()`
- Purpose: Gets the maximum screen size for a specific LOD level.
- Calls: None (directly).

## Globals
- **MAX_RANDOM_ENTRIES (const unsigned int)**: Maximum size of randomizer tables (must be power of two).
- **rand_gen (static Random4Class)**: Random number generator instance.
- **oo_intmax (const float)**: Reciprocal of INT_MAX for normalization.
- **TotalActiveCount (unsigned int)**: Tracks total active particle buffers.
- **LODMaxScreenSizes (float[17])**: Screen-size clamps for LOD levels.

## Dependencies
- **Headers**: `part_buf.h`, `part_emt.h`, `ww3d.h`, `rinfo.h`, `scene.h`, `camera.h`, `predlod.h`, `pot.h`, `bound.h`, `simplevec.h`, `sphere.h`, `wwprofile.h`, `vp.h`, `texture.h`, `dx8wrapper.h`, `vector3.h`.
- **External Symbols**: `WW3D::Get_Sync_Time()`, `NEW_REF`, `W3DNEW`, `W3DNEWARRAY`, `MIN`, `NO_MAX_S
