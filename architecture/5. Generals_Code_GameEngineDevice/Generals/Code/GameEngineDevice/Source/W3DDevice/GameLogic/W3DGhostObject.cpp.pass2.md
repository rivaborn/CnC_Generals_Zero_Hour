# Generals/Code/GameEngineDevice/Source/W3DDevice/GameLogic/W3DGhostObject.cpp - Enhanced Analysis

## Architectural Role
This file implements the fog-of-war visualization system by managing "ghost" representations of objects that are obscured by fog. It bridges the game logic layer (Object, PartitionManager) with the rendering layer (W3DDevice) to maintain visual consistency during fog transitions.

## Cross-References
### Incoming
- **GameLogic**: Object::friend_getPartitionData() calls into W3DGhostObjectManager during player transitions
- **PartitionManager**: Registers ghost objects via ThePartitionManager->registerGhostObject()
- **Xfer**: Serialization system calls crc/xfer/loadPostProcess during save/load

### Outgoing
- **W3DDevice**: Uses W3DModelDraw, W3DAssetManager, W3DDisplay for render object management
- **WW3D2**: Directly manipulates RenderObjClass, HLodClass, MaterialInfoClass for visual state
- **GameClient**: Interacts with DrawableInfo for scene integration

## Design Patterns
- **Snapshot Pattern**: W3DRenderObjectSnapshot captures and restores render object state for fog transitions
- **Proxy Pattern**: Ghost objects act as proxies for real objects when fogged
- **Material Override**: Uses static animationDisableOverride to disable texture animations on ghosts (performance optimization)
