# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_emt.h - Enhanced Analysis

## Architectural Role
This file defines the core particle emitter system in the W3D rendering engine, bridging between high-level effect definitions and low-level particle rendering. It manages particle generation, property interpolation, and buffer synchronization, serving as the primary interface for particle effects in the game.

## Cross-References
### Incoming
- **part_buf.h**: Uses `ParticleBufferClass` for particle storage and rendering
- **rendobj.h**: Inherits from `RenderObjClass` for scene integration
- **w3d_file.h**: Likely used for serialization of emitter definitions
- **Scene management**: Called by scene systems to handle emitter visibility and updates

### Outgoing
- **part_buf.h**: Delegates particle rendering and buffer management
- **random.h**: Uses randomizers for particle position/velocity variation
- **quat.h**: Applies quaternion transformations for particle orientation
- **v3_rnd.h**: Handles vector3 randomizations for particle properties

## Design Patterns
- **Composite**: Emitter manages a collection of particles (via buffer) as a single unit
- **Template Method**: Keyframe interpolation follows a standardized pattern for different property types
- **Observer**: Notifies scene when added/removed via `Notify_Added`/`Notify_Removed`

*Not inferable*: Exact factory pattern usage for emitter creation (e.g., `Create_From_Definition`)
