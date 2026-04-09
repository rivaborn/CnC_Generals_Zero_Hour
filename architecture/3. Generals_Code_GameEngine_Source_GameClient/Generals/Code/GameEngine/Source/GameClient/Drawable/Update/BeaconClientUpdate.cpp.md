# Generals/Code/GameEngine/Source/GameClient/Drawable/Update/BeaconClientUpdate.cpp

## Purpose
Handles client-side updates for beacon objects, including particle effects and radar pulses.

## Responsibilities
- Manages beacon visibility and particle system creation
- Controls radar pulse events based on timing parameters
- Serializes beacon state for network synchronization
- Configures beacon behavior via INI file parsing

## Key Types
- **BeaconClientUpdateModuleData (Class)**: Stores beacon update parameters (radar pulse frequency/duration)
- **BeaconClientUpdate (Class)**: Implements beacon client update logic
- **ParticleSystemID (Type)**: Identifier for particle systems

## Key Functions
### createParticleSystem
- Purpose: Creates and attaches a particle system to a beacon drawable
- Calls: `TheParticleSystemManager->findTemplate`, `TheParticleSystemManager->createParticleSystem`, `system->attachToDrawable`, `system->tintAllColors`

### hideBeacon
- Purpose: Hides beacon and stops its particle system
- Calls: `getDrawable`, `draw->setDrawableHidden`, `draw->setShadowsEnabled`, `createParticleSystem`, `TheParticleSystemManager->findParticleSystem`, `system->stop`

### clientUpdate
- Purpose: Handles periodic beacon updates including radar pulses
- Calls: `getDrawable`, `createParticleSystem`, `TheRadar->createEvent`

## Globals
- None

## Dependencies
- `Drawable.h`, `ParticleSys.h`, `BeaconClientUpdate.h`, `Player.h`, `PlayerList.h`, `Radar.h`, `Xfer.h`, `GameLogic.h`
- `TheParticleSystemManager`, `TheRadar`, `TheGameLogic`
