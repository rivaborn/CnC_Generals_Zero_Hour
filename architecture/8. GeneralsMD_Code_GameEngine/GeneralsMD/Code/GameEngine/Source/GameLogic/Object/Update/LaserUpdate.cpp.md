# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/LaserUpdate.cpp

## Purpose
Handles laser update processing for render purposes and game control in the SAGE engine.

## Responsibilities
- Manages laser start/end position updates
- Controls laser width animation (widening/decaying)
- Handles particle system creation and positioning for laser effects
- Manages laser state across network transfers
- Tracks parent/child relationships for laser rendering

## Key Types
- **LaserUpdateModuleData (Class)**: Stores laser configuration data (particle systems, punch-through scalar)
- **LaserUpdate (Class)**: Main laser update module handling position tracking and animation
- **None**: No enums/structs defined

## Key Functions
### `updateStartPos()`
- Purpose: Updates the laser's starting position based on parent object or bone
- Calls: `getCurrentWorldspaceClientBonePositions`, `getPosition`

### `updateEndPos()`
- Purpose: Updates the laser's ending position based on target object or punch-through logic
- Calls: `findDrawableByID`, `getObject`, `isEffectivelyDead`, `getPosition`

### `clientUpdate()`
- Purpose: Main update loop handling position updates and width animations
- Calls: `updateStartPos`, `updateEndPos`, `getFrame`

### `initLaser()`
- Purpose: Initializes laser with parent/target objects and particle systems
- Calls: `findTemplate`, `createParticleSystem`, `getSystemID`, `setPosition`, `destroyDrawable`

### `xfer()`
- Purpose: Serializes laser state for network transfer
- Calls: `xferVersion`, `xferCoord3D`, `xferBool`, `xferUser`, `xferUnsignedInt`, `xferReal`, `xferDrawableID`, `xferAsciiString`

## Globals
- **TheParticleSystemManager (External)**: Manages particle systems
- **TheGameClient (External)**: Client-side game interface
- **TheGameLogic (External)**: Game logic interface
- **ThePlayerList (External)**: Player management

## Dependencies
- Common: `Player.h`, `PlayerList.h`, `Xfer.h`, `DrawModule.h`, `ThingTemplate.h`
- GameClient: `Drawable.h`, `GameClient.h`, `ParticleSys.h`
- GameLogic: `Object.h`, `GameLogic.h`
- Module: `LaserUpdate.h`
- WWMath: `Vector3.h`
