# GeneralsMD/Code/GameEngine/Include/GameClient/ParticleSys.h

## Purpose
Defines particle system classes and types for rendering visual effects in the game.

## Responsibilities
- Declares particle system hierarchy (Particle, ParticleSystem, ParticleSystemManager)
- Defines particle properties, emission volumes, and rendering parameters
- Provides template system for particle system instantiation
- Manages particle system lifecycle and rendering priorities

## Key Types
- **Particle (Class)**: Individual particle with position, velocity, and lifetime
- **ParticleSystem (Class)**: Manages particle emission and behavior
- **ParticleSystemManager (Class)**: Global manager for all particle systems
- **ParticlePriorityType (Enum)**: Priority levels for particle rendering
- **ParticleSystemInfo (Class)**: Base class containing particle system properties
- **ParticleSystemTemplate (Class)**: Template for creating particle systems

## Key Functions
### ParticleSystem::update
- Purpose: Updates particle system state and emits new particles
- Calls: generateParticleInfo, computeParticlePosition, computeParticleVelocity

### ParticleSystemManager::createParticleSystem
- Purpose: Instantiates a particle system from a template
- Calls: ParticleSystem constructor

### ParticleSystem::generateParticleInfo
- Purpose: Generates random particle properties for emission
- Calls: None visible in header

## Globals
- **TheParticleSystemManager (ParticleSystemManager*)**: Singleton instance of the manager

## Dependencies
- Common GameEngine types (AsciiString, MemoryPoolObject)
- WWMath Matrix3D
- INI parsing infrastructure
- Snapshot system for serialization
- STL containers (list, hash_map)
