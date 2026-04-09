# GeneralsMD/Code/GameEngine/Source/GameClient/Drawable/Update/AnimatedParticleSysBoneClientUpdate.cpp

## Purpose
Handles client-side updates for animated particle systems attached to bones in 3D models.

## Responsibilities
- Manages particle system updates tied to skeletal animation
- Increments a life counter for timing purposes
- Calls bone update methods on draw modules
- Implements serialization (Xfer) and CRC for network sync

## Key Types
- `AnimatedParticleSysBoneClientUpdate` (Class): Client update module for bone-attached particle systems

## Key Functions
### `clientUpdate`
- Purpose: Updates particle systems based on bone transformations
- Calls: `getDrawable`, `getDrawModules`, `getObjectDrawInterface`, `updateBonesForClientParticleSystems`

### `crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `ClientUpdateModule::crc`

### `xfer`
- Purpose: Serializes/deserializes module state
- Calls: `ClientUpdateModule::xfer`, `xferVersion`

### `loadPostProcess`
- Purpose: Post-processing after loading
- Calls: `ClientUpdateModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Drawable.h`, `AnimatedParticleSysBoneClientUpdate.h`, `Player.h`, `PlayerList.h`, `ThingFactory.h`, `ThingTemplate.h`, `RandomValue.h`, `DrawModule.h`, `PerfTimer.h`, `Xfer.h`, `Object.h`, `ScriptEngine.h`
- `ClientUpdateModule`, `Thing`, `ModuleData`, `Drawable`, `DrawModule`, `ObjectDrawInterface`, `Xfer`, `XferVersion`
