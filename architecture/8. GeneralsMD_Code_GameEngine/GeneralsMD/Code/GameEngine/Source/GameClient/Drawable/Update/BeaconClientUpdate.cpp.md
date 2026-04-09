# GeneralsMD/Code/GameEngine/Source/GameClient/Drawable/Update/BeaconClientUpdate.cpp

## Purpose
Handles client-side updates for beacon objects, including particle effects and radar pulses.

## Responsibilities
- Manages beacon visibility and particle system creation
- Controls radar pulse events based on timing parameters
- Serializes beacon state for network synchronization
- Loads module-specific data from configuration

## Key Types
- **BeaconClientUpdateModuleData (Class)**: Stores configuration for radar pulse frequency and duration
- **BeaconClientUpdate (Class)**: Implements client-side beacon behavior
- **ParticleSystemID (Type)**: Identifier for particle effects

## Key Functions
### createParticleSystem
- Purpose: Creates and attaches a particle system to the beacon drawable
- Calls: `TheParticleSystemManager->findTemplate`, `TheParticleSystemManager->createParticleSystem`, `system->attachToDrawable`, `system->tintAllColors`

### hideBeacon
- Purpose: Hides the beacon and stops its particle system
- Calls: `getDrawable`, `draw->setDrawableHidden`, `draw->setShadowsEnabled`, `createParticleSystem`, `TheParticleSystemManager->findParticleSystem`, `system->stop`

### clientUpdate
- Purpose: Updates beacon state each frame, including radar pulses
- Calls: `getDrawable`, `createParticleSystem`, `TheRadar->createEvent`, `TheGameLogic->getFrame`

### xfer
- Purpose: Serializes beacon state for network transfer
- Calls: `ClientUpdateModule::xfer`, `xfer->xferUser`, `xfer->xferUnsignedInt`

## Globals
- **TheParticleSystemManager (External)**: Manages particle system templates and instances
- **TheRadar (External)**: Handles radar event creation
- **TheGameLogic (External)**: Provides game timing information

## Dependencies
- `GameClient/Drawable.h`, `GameClient/ParticleSys.h`, `GameClient/Module/BeaconClientUpdate.h`
- `Common/Player.h`, `Common/PlayerList.h`, `Common/Radar.h`, `Common/Xfer.h`
- `GameLogic/GameLogic.h`
