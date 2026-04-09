# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StickyBombUpdate.cpp

## Purpose
Handles the logic for sticky bombs, making them follow targets and detonate after a set time or remotely.

## Responsibilities
- Tracks target objects and updates bomb position to follow them
- Manages bomb lifetime and detonation timing
- Plays audio cues (creation and countdown pings)
- Handles geometry-based damage calculations on detonation
- Manages booby trap status for targeted objects

## Key Types
- **StickyBombUpdate (Class)**: Manages sticky bomb behavior and updates
- **StickyBombUpdateModuleData (Struct)**: Configuration data for sticky bomb behavior (referenced but not defined here)

## Key Functions
### `initStickyBomb`
- Purpose: Initializes bomb targeting and timing parameters
- Calls: `getObject()`, `findObjectByID()`, `getAIUpdateInterface()`, `getGoalObject()`, `findUpdateModule()`, `getDieFrame()`, `setWakeFrame()`, `getPosition()`, `getGroundHeight()`, `setPosition()`, `setStatus()`, `getPerUnitSound()`, `addAudioEvent()`

### `update`
- Purpose: Updates bomb position to follow target and handles countdown sounds
- Calls: `getTargetObject()`, `isEffectivelyDead()`, `destroyObject()`, `getPosition()`, `getGroundHeight()`, `setPosition()`, `getFrame()`, `getPerUnitSound()`, `addAudioEvent()`

### `detonate`
- Purpose: Handles bomb detonation, damage calculation, and effects
- Calls: `getTargetObject()`, `getGeometryInfo()`, `getBoundingCircleRadius()`, `getPrimaryDamage()`, `getSecondaryDamage()`, `getPrimaryDamageRadius()`, `getSecondaryDamageRadius()`, `iterateObjectsInRange()`, `firstWithNumeric()`, `nextWithNumeric()`, `attemptDamage()`, `doFXPos()`, `clearStatus()`, `kill()`

### `xfer`
- Purpose: Serializes bomb state for network synchronization
- Calls: `UpdateModule::xfer()`, `xferObjectID()`, `xferUnsignedInt()`

## Globals
- **m_targetID (ObjectID)**: Stores the ID of the targeted object
- **m_dieFrame (UnsignedInt)**: Frame when bomb should detonate
- **m_nextPingFrame (UnsignedInt)**: Next frame for countdown sound

## Dependencies
- Key includes: `PreRTS.h`, `StickyBombUpdate.h`, `ThingTemplate.h`, `Player.h`, `Xfer.h`, `Drawable.h`, `FXList.h`, `InGameUI.h`, `Object.h`, `ObjectIter.h`, `PartitionManager.h`, `Weapon.h`, `LifetimeUpdate.h`, `AIUpdate.h`, `BodyModule.h`, `GameLogic.h`
- External symbols: `TheGameLogic`, `
