# Generals/Code/GameEngine/Source/GameClient/System/ParticleSys.cpp

## Purpose
Implements the particle system manager and related classes for visual effects in the game.

## Responsibilities
- Manages particle systems and templates
- Handles particle creation, updating, and destruction
- Provides debugging display for particle statistics
- Manages particle system assets and networking

## Key Types
- ParticleInfo (Struct): Contains particle properties like velocity, position, and lifetime
- Particle (Class): Represents an individual particle with behavior and rendering
- ParticleSystemManager (Class): Singleton manager for all particle systems
- ParticleSystemTemplate (Class): Template for creating particle systems
- (anonymous enum): Contains MAX_SIZE_BONUS constant

## Key Functions
### ParticleSystemDebugDisplay
- Purpose: Displays particle system statistics on screen
- Calls: TheParticleSystemManager->getParticleCount(), getOnScreenParticleCount(), getParticleSystemCount(), getAllParticleSystems()

## Globals
- TheParticleSystemManager (ParticleSystemManager*): Singleton instance of the particle system manager

## Dependencies
- Common/GameState.h, Common/INI.h, Common/PerfTimer.h, Common/ThingFactory.h, Common/GameLOD.h, Common/Xfer.h
- GameClient/Drawable.h, GameClient/DebugDisplay.h, GameClient/Display.h, GameClient/GameClient.h, GameClient/InGameUI.h, GameClient/ParticleSys.h
- GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/TerrainLogic.h
