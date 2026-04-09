# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DParticleSys.h

## Purpose
Header for the W3D particle system manager, handling particle rendering and management in the game engine.

## Responsibilities
- Manages particle systems and streaks in the W3D rendering pipeline
- Handles particle rendering queueing and execution
- Tracks on-screen particle count for performance metrics
- Maintains buffers for particle properties (position, color, size, orientation)

## Key Types
- **W3DParticleSystemManager (Class)**: Manages particle systems and rendering in W3D.
- **(anonymous enum) (Enum)**: Defines `MAX_POINTS_PER_GROUP` constant.
- **MAX_POINTS_PER_GROUP (Enum)**: Maximum points per particle group (512).

## Key Functions
### W3DParticleSystemManager()
- Purpose: Constructor for the particle system manager.
- Calls: Not inferable.

### ~W3DParticleSystemManager()
- Purpose: Destructor for the particle system manager.
- Calls: Not inferable.

### doParticles(RenderInfoClass &rinfo)
- Purpose: Processes and renders particles for a given frame.
- Calls: Not inferable.

### queueParticleRender()
- Purpose: Queues particle rendering for the next frame.
- Calls: Not inferable.

### getOnScreenParticleCount()
- Purpose: Returns the number of particles rendered on-screen per frame.
- Calls: Not inferable.

## Globals
- **m_pointGroup (PointGroupClass*)**: Stores all particles.
- **m_streakLine (StreakLineClass*)**: Stores all streaks.
- **m_posBuffer (ShareBufferClass<Vector3>*)**: Buffer for particle positions.
- **m_RGBABuffer (ShareBufferClass<Vector4>*)**: Buffer for particle colors and alpha.
- **m_sizeBuffer (
