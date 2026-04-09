# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_buf.cpp

## Purpose
Manages particle buffer rendering and lifecycle in the SAGE engine, handling particle properties, LOD, and various render modes.

## Responsibilities
- Manages particle buffers with circular buffer architecture
- Handles particle properties (color, opacity, size, rotation, etc.)
- Implements LOD (Level of Detail) for performance optimization
- Supports multiple render modes (tri/quad particles, lines, line groups)
- Manages particle keyframes and randomizers

## Key Types
- **ParticleBufferClass**: Main class managing particle buffers
- **ParticlePropertyStruct<T>**: Template struct for particle properties
- **W3dEmitterLinePropertiesStruct**: Line emitter properties
- **TailDiffuseTypeEnum**: Enum for tail diffuse types

## Key Functions
### ParticleBufferClass()
- Purpose: Constructor initializing particle buffer
- Calls: Reset_Colors, Reset_Opacity, Reset_Size, Reset_Rotations, Reset_Frames, Reset_Blur_Times

### Update()
- Purpose: Updates particle buffer state
- Calls: Not inferable (truncated)

### Render()
- Purpose: Renders particle buffer
- Calls: Not inferable (truncated)

### Get_Size_Key_Frames()
- Purpose: Retrieves size keyframes
- Calls: None

### Get_Rotation_Key_Frames()
- Purpose: Retrieves rotation keyframes
- Calls: None

### Get_Frame_Key_Frames()
- Purpose: Retrieves frame keyframes
- Calls: None

### Get_Blur_Time_Key_Frames()
- Purpose: Retrieves blur time keyframes
- Calls: None

### Set_LOD_Max_Screen_Size()
- Purpose: Sets LOD max screen size
- Calls: None

### Get_LOD_Max_Screen_Size()
- Purpose: Gets LOD max screen size
- Calls: None

### Determine_Tail_Diffuse()
- Purpose: Determines tail diffuse type
- Calls: Get_Texture, Get_Shader

### Get_Texture()
- Purpose: Gets particle texture
- Calls: None

### Set_Texture()
- Purpose: Sets particle texture
- Calls: None

### Get_Shader()
- Purpose: Gets particle shader
- Calls: None

## Globals
- **MAX_RANDOM_ENTRIES (unsigned int)**: Maximum size of randomizer tables
- **rand_gen (Random4Class)**: Random number generator
- **oo_intmax (float)**: Reciprocal of INT_MAX
- **_DefaultLineEmitterProps (W3dEmitterLinePropertiesStruct)**: Default line emitter properties

## Dependencies
- Key includes: part_buf.h, part_emt.h, ww3d.h, rinfo.h, scene.h, camera.h, predlod.h, pot.h, bound.h, simplevec.h, sphere.h, wwprofile.h, vp.h, texture.h, dx8wrapper.h, vector3.h
- External symbols: W3DNEW, W3DNEWARRAY, NEW_REF, REF_PTR_RELEASE, WWASSERT, WW3D::Get_Sync_Time()
