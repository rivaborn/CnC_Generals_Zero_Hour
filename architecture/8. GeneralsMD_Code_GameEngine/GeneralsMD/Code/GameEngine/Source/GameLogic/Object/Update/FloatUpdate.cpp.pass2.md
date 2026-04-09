# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FloatUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the floating behavior for objects in the game, bridging the game logic layer with the rendering system. It adjusts object positions to match water surface height and applies visual floating animations, critical for units like boats or structures near water.

## Cross-References
### Incoming
- **GameLogic/Object.h**: Uses `Thing` base class and position/drawable accessors
- **GameClient/Drawable.h**: Manipulates object transformation matrices for animation
- **GameLogic/TerrainLogic.h**: Queries water height via `isUnderwater()`
- **GameLogic/GameLogic.h**: Accesses frame counter for animation timing

### Outgoing
- **Common/Xfer.h**: Handles network serialization/deserialization
- **GameLogic/Module/FloatUpdate.h**: Defines module data and interface
- **UpdateModule** (base class): Extends core update module functionality

## Design Patterns
- **Strategy Pattern**: `FloatUpdate` is a concrete strategy for object behavior, pluggable via the `UpdateModule` interface
- **Observer Pattern**: Reacts to terrain changes (water height) without direct coupling
- **Template Method**: `xfer()` and `crc()` follow base class templates for serialization consistency

*Not inferable*: No clear use of Visitor, Factory, or Decorator patterns.
