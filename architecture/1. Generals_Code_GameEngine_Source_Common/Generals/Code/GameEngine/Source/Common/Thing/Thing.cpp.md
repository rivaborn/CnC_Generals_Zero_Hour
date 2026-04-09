# Generals/Code/GameEngine/Source/Common/Thing/Thing.cpp

## Purpose
This file contains the implementation of the `Thing` class, which serves as a base class for objects and drawables in the game engine. It handles common data and operations related to these entities.

## Responsibilities
- Manage transformation matrices and position updates.
- Provide methods to get direction vectors and orientation.
- Cache altitude calculations for performance optimization.
- Handle interactions with terrain logic.

## Key Types
- `Thing` (Class): Base class for objects and drawables, managing common properties and transformations.
- `Coord3D` (Struct): Represents 3D coordinates.
- `Matrix3D` (Class): Represents a 3x3 transformation matrix.
- `KindOfType` (Enum): Defines types of game entities.

## Key Functions
### Thing::Thing
- Purpose: Constructor for the `Thing` class, initializes with a template and sets default values.
- Calls: None

### Thing::~Thing
- Purpose: Destructor for the `Thing` class.
- Calls: None

### Thing::getTemplate
- Purpose: Returns the template associated with the `Thing`.
- Calls: None

### Thing::getUnitDirectionVector2D
- Purpose: Calculates and returns a 2D unit direction vector based on orientation.
- Calls: Cos, Sin

### Thing::setPositionZ
- Purpose: Sets the Z position of the `Thing`, handling terrain alignment if necessary.
- Calls: TheTerrainLogic->alignOnTerrain, reactToTransformChange

### Thing::setPosition
- Purpose: Sets the 3D position of the `Thing`, handling terrain alignment if necessary.
- Calls: TheTerrainLogic->alignOnTerrain, reactToTransformChange

### Thing::setOrientation
- Purpose: Sets the orientation (angle) of the `Thing`, updating transformation matrix and direction vector.
- Calls: Cos, Sin, TheTerrainLogic->alignOnTerrain, reactToTransformChange

### Thing::setTransformMatrix
- Purpose: Sets the world transformation matrix for the `Thing`.
- Calls: reactToTransformChange

### Thing::calculateHeightAboveTerrain
- Purpose: Calculates the height of the `Thing` above the terrain.
- Calls: TheTerrainLogic->getGroundHeight

### Thing::getHeightAboveTerrain
- Purpose: Returns cached or calculated height above terrain.
- Calls: calculateHeightAboveTerrain

### Thing::transformPoint
- Purpose: Transforms a point from local to world coordinates using the transformation matrix.
- Calls: m_transform.Transform_Vector

## Globals
- None

## Dependencies
- `Common/PerfTimer.h`
- `Common/Thing.h`
- `Common/ThingTemplate.h`
- `Common/ThingFactory.h`
- `Common/GlobalData.h`
- `Common/NameKeyGenerator.h`
- `Common/Player.h`
- `Common/PlayerList.h`
- `
