# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_emt.cpp - Enhanced Analysis

## Architectural Role
This file implements the core particle emitter system in the SAGE engine's rendering pipeline. It bridges between high-level emitter definitions and low-level particle rendering, managing the lifecycle of particle systems used for visual effects like explosions, smoke, and debris.

## Cross-References
### Incoming
- **part_ldr.cpp**: Calls `Create_From_Definition` to instantiate emitters from definitions
- **SceneClass**: Invokes `On_Frame_Update` during scene rendering
- **AssetManager**: Used for texture loading in emitter creation

### Outgoing
- **ParticleBufferClass**: Delegates particle storage and rendering
- **TextureClass**: For texture management and dependency tracking
- **SceneClass**: Registers/unregisters emitters for scene management

## Design Patterns
- **Factory Pattern**: `Create_From_Definition` creates emitter instances from definitions
- **Observer Pattern**: Emitters respond to scene visibility changes via `Update_On_Visibilty`
- **Property Container**: Uses `ParticlePropertyStruct` for keyframe-based animation data

*Not inferable: Exact template usage patterns for `ParticlePropertyStruct`*
