# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DParticleSys.h

## Purpose
Header for the W3D particle system manager, handling particle rendering and updates in the game engine.

## Responsibilities
- Manages particle system rendering via W3D
- Handles particle position, color, size, and orientation buffers
- Tracks on-screen particle count
- Queues particle rendering operations

## Key Types
- **W3DParticleSystemManager (Class)**: Manages particle systems for W3D rendering.
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
- Purpose: Updates and renders particles for a given frame.
- Calls: Not inferable.

### queueParticleRender()
- Purpose: Queues particle rendering operations.
- Calls: Not inferable.

### getOnScreenParticleCount()
- Purpose: Returns the number of particles shown on screen per frame.
- Calls: Not inferable.

## Globals
- **m_pointGroup (PointGroupClass*)**: The point group containing all particles.
- **m_streakLine (StreakLineClass*)**: The streak class containing all streaks.
- **m_posBuffer (ShareBufferClass<Vector3>*)**: Array of particle positions.
- **m_RGBABuffer (ShareBufferClass<Vector4>*)**: Array of particle colors and alpha.
- **m_sizeBuffer (ShareBufferClass<float>*)**: Array of particle sizes
