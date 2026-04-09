# Generals/Code/GameEngine/Source/GameLogic/Object/Update/LaserUpdate.cpp

## Purpose
Handles laser update processing for render purposes and game control.

## Responsibilities
- Manages laser initialization, including position and particle systems.
- Updates laser width during widening or decaying phases.
- Handles cleanup of particle systems on destruction.

## Key Types
- **LaserUpdateModuleData (Struct)**: Stores data for laser module configuration.
- **LaserUpdate (Class)**: Manages the update logic for lasers.

## Key Functions
### LaserUpdate::clientUpdate
- Purpose: Updates the laser's width during widening or decaying phases.
- Calls:
  - TheGameLogic->getFrame()
  - TheParticleSystemManager->destroyParticleSystemByID()

### LaserUpdate::setDecayFrames
- Purpose: Sets up the decay phase for the laser.
- Calls:
  - TheGameLogic->getFrame()

### LaserUpdate::initLaser
- Purpose: Initializes the laser's start and end positions, and sets up particle systems.
- Calls:
  - getSingleLogicalBonePositionOnTurret()
  - getSingleLogicalBonePosition()
  - TheParticleSystemManager->findTemplate()
  - TheParticleSystemManager->createParticleSystem()
  - setPosition()

### LaserUpdate::getCurrentLaserRadius
- Purpose: Returns the current radius of the laser based on its width scalar.
- Calls:
  - getDrawable()->getDrawModules()
  - getLaserDrawInterface()
  - getLaserTemplateWidth()

## Globals
None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "Common/DrawModule.h"
  - "GameClient/Drawable.h"
  - "GameClient/GameClient.h"
  - "GameClient/ParticleSys.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/LaserUpdate.h"
  - "WWMath/Vector3.h"

- **External Symbols**:
  - TheParticleSystemManager
  - TheGameLogic
  - TheGameClient
