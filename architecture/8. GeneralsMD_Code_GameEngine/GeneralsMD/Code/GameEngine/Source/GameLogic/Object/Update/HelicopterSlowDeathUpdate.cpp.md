# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HelicopterSlowDeathUpdate.cpp

## Purpose
Implements the slow death behavior for helicopters, including spiral descent, blade detachment, and final explosion effects.

## Responsibilities
- Manages helicopter death animation sequence (spiral descent, blade fly-off, ground impact, final explosion)
- Handles particle effects, sound, and object creation during death sequence
- Controls physics forces (lift, braking) during descent
- Spawns rubble object after final destruction
- Synchronizes with game logic and terrain collision

## Key Types
- `HelicopterSlowDeathBehaviorModuleData` (struct): Configuration data for helicopter death behavior (spiral rates, delays, effects)
- `HelicopterSlowDeathBehavior` (class): Module implementing helicopter slow death logic
- `SlowDeathBehavior` (class): Base class for slow death behaviors

## Key Functions
### `beginSlowDeath`
- Purpose: Initializes helicopter death sequence with spiral parameters and effects
- Calls: `SlowDeathBehavior::beginSlowDeath`, `TheAudio->addAudioEvent`, `TheParticleSystemManager->createParticleSystem`

### `update`
- Purpose: Updates helicopter death animation frame-by-frame (spiral motion, blade detachment, ground impact, final explosion)
- Calls: `SlowDeathBehavior::update`, `TheGameLogic->getFrame`, `TheTerrainLogic->getLayerHeight`, `FXList::doFXObj`, `ObjectCreationList::create`, `TheGameLogic->destroyObject`

### `xfer`
- Purpose: Serializes/deserializes module state for network sync
- Calls: `SlowDeathBehavior::xfer`, `Xfer::xferVersion`, `Xfer::xferInt`, `Xfer::xferReal`, `Xfer::xferBool`, `Xfer::xferUnsignedInt`

## Globals
- `ORBIT_DIRECTION_LEFT` (const float): Direction constant for spiral orbit
- `ORBIT_DIRECTION_RIGHT` (const float): Direction constant for spiral orbit

## Dependencies
- GameLogic modules: `SlowDeathBehavior`, `PhysicsBehavior`, `EjectPilotDie`
- GameClient: `Drawable`, `ParticleSystem`, `FXList`
- Common: `GameAudio`, `ThingFactory`, `ObjectCreationList`
- External: `TheGameLogic`, `TheTerrainLogic`, `TheAudio`, `TheParticleSystemManager`
