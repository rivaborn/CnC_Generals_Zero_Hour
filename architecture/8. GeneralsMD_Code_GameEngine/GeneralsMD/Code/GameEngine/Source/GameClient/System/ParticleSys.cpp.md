# GeneralsMD/Code/GameEngine/Source/GameClient/System/ParticleSys.cpp

## Purpose
Implements the particle system manager and related classes for rendering visual effects in the game.

## Responsibilities
- Manages particle systems and individual particles
- Handles particle creation, updating, and rendering
- Provides debugging display for particle statistics
- Manages particle system templates and their instantiation

## Key Types
- ParticleInfo (Struct): Contains particle properties like velocity, position, and lifetime
- Particle (Class): Represents an individual particle with behavior and rendering
- ParticleSystemManager (Class): Singleton manager for all particle systems
- ParticleSystemTemplate (Class): Template for creating particle systems

## Key Functions
### ParticleSystemDebugDisplay
- Purpose: Displays particle system statistics in the debug interface
- Calls: TheParticleSystemManager->getParticleCount(), getOnScreenParticleCount(), getParticleSystemCount()

### angleBetween
- Purpose: Calculates the angle between two 2D vectors
- Calls: None (math operations only)

## Globals
- TheParticleSystemManager (ParticleSystemManager*): Singleton instance of the particle system manager

## Dependencies
- Common/GameState.h, Common/INI.h, Common/PerfTimer.h, Common/ThingFactory.h, Common/GameLOD.h, Common/Xfer.h
- GameClient/Drawable.h, GameClient/DebugDisplay.h, GameClient/Display.h, GameClient/GameClient.h, GameClient/InGameUI.h, GameClient/ParticleSys.h
- GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/TerrainLogic.h
