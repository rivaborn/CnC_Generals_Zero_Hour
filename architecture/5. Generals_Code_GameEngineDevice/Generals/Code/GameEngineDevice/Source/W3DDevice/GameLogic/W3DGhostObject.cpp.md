# Generals/Code/GameEngineDevice/Source/W3DDevice/GameLogic/W3DGhostObject.cpp

## Purpose
Manages "ghost" objects that represent fogged-out game objects, maintaining their visual state for players who haven't yet uncovered them.

## Responsibilities
- Creates and maintains snapshots of render objects for fogged-out game objects
- Handles transitions between real objects and their ghost representations
- Manages ghost object lifecycle during game state changes (loading, player switching)
- Disables texture animations on ghost objects for performance

## Key Types
- **W3DRenderObjectSnapshot (Class)**: Stores snapshot of a render object's state for fogged representation
- **W3DGhostObject (Class)**: Manages ghost object state and transitions (defined in header)
- **W3DGhostObjectManager (Class)**: System-wide manager for ghost objects (defined in header)
- **animationDisableOverride (RenderObjClass::Material_Override)**: Static material override to disable UV animations

## Key Functions
### disableUVAnimations
- Purpose: Disables texture scrolling animations on HLOD render objects
- Calls: None (directly manipulates W3D render object properties)

### W3DRenderObjectSnapshot::update
- Purpose: Refreshes the snapshot with current render object state
- Calls: disableUVAnimations, RenderObjClass methods (Clone, Set_Transform, etc.)

### W3DGhostObject::snapShot
- Purpose: Captures current state of object's render objects when entering fogged state
- Calls: W3DRenderObjectSnapshot constructor/update, RenderObjClass::Remove

### W3DGhostObjectManager::setLocalPlayerIndex
- Purpose: Handles ghost object transitions when switching between players
- Calls: W3DGhostObject::removeFromScene, addToScene, restoreParentObject

## Globals
- **animationDisableOverride (RenderObjClass::Material_Override)**: Material override to disable texture animations on ghost objects

## Dependencies
- Common: Debug, Player, PlayerList, ThingTemplate, Xfer
- GameClient: Drawable, GameClient
- GameLogic: GameLogic, Object, PartitionManager
- W3DDevice: W3DModelDraw, W3DAssetManager, W3DDisplay
- WW3D2: rendobj, hlod, Scene, matinfo
- Snapshot base class for serialization
