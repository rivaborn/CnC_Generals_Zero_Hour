# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameLogic/W3DGhostObject.cpp

## Purpose
Manages "ghost" objects that represent fogged-out game objects, maintaining their visual state for players who cannot see them directly.

## Responsibilities
- Creates and maintains snapshots of render objects for fogged-out game objects
- Handles transitions between real and ghost representations when objects enter/exit fog
- Manages ghost object lifecycle (creation, updates, removal)
- Supports network synchronization of ghost objects
- Disables animations/texture effects on ghost objects

## Key Types
- **W3DRenderObjectSnapshot (Class)**: Stores snapshot of a render object's state for fogged representation
- **W3DGhostObject (Class)**: Manages ghost representation of a game object
- **W3DGhostObjectManager (Class)**: System-wide manager for all ghost objects

## Key Functions
### disableUVAnimations
- Purpose: Disables texture animations and muzzle effects on ghost objects
- Calls: None (directly manipulates render object properties)

### W3DRenderObjectSnapshot::update
- Purpose: Updates the snapshot with current render object state
- Calls: disableUVAnimations

### W3DGhostObject::snapShot
- Purpose: Creates snapshot of object when it enters fogged state
- Calls: W3DRenderObjectSnapshot constructor, disableUVAnimations

### W3DGhostObjectManager::addGhostObject
- Purpose: Creates new ghost object for tracking
- Calls: None (manages internal linked list)

## Globals
- **animationDisableOverride (RenderObjClass::Material_Override)**: Material override to disable animations on ghost objects

## Dependencies
- Common/Debug.h, Common/Player.h, Common/PlayerList.h, Common/ThingTemplate.h, Common/Xfer.h
- GameClient/Drawable.h, GameClient/GameClient.h, GameLogic/GameLogic.h, GameLogic/Object.h
- GameLogic/PartitionManager.h, W3DDevice/GameClient/Module/W3DModelDraw.h
- W3DDevice/GameClient/W3DAssetManager.h, W3DDevice/GameClient/W3DDisplay.h
- W3DDevice/GameLogic/W3DGhostObject.h, WW3D2/rendobj.h, WW3D2/hlod.h, WW3D2/Scene.h, WW3D2/matinfo.h
