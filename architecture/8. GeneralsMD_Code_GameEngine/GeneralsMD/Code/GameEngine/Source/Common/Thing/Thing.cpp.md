# GeneralsMD/Code/GameEngine/Source/Common/Thing/Thing.cpp

## Purpose
Implements the `Thing` base class, which serves as a common foundation for both game objects (logic-side) and drawables (client-side) in the SAGE engine.

## Responsibilities
- Manages spatial transformation (position, orientation, matrix)
- Caches derived values (direction vectors, height above terrain)
- Provides template-based type checking
- Handles terrain alignment for slope-sticking objects
- Supports coordinate system conversions

## Key Types
- `Thing` (Class): Base class for game entities with shared spatial data
- `ThingTemplate` (Pointer): Reference to the entity's template definition

## Key Functions
### `Thing::Thing(const ThingTemplate *thingTemplate)`
- Purpose: Constructs a Thing from a template.
- Calls: None (initializes member variables)

### `Thing::setPositionZ(Real z)`
- Purpose: Sets the Z-coordinate, handling terrain alignment if needed.
- Calls: `TheTerrainLogic->alignOnTerrain()`, `setTransformMatrix()`, `reactToTransformChange()`

### `Thing::setOrientation(Real angle)`
- Purpose: Rotates the Thing around the Z-axis, with terrain alignment if required.
- Calls: `TheTerrainLogic->alignOnTerrain()`, `reactToTransformChange()`

### `Thing::setTransformMatrix(const Matrix3D *mx)`
- Purpose: Applies a full 3D transformation matrix.
- Calls: `reactToTransformChange()`

### `Thing::getHeightAboveTerrain() const`
- Purpose: Returns cached or calculated height above terrain.
- Calls: `calculateHeightAboveTerrain()`, `TheTerrainLogic->getGroundHeight()`

### `Thing::transformPoint(const Coord3D *in, Coord3D *out)`
- Purpose: Transforms a point through the Thing's matrix.
- Calls: None (uses `Matrix3D::Transform_Vector`)

## Globals
- `TheTerrainLogic` (External): Terrain system singleton for height queries
- `TheGlobalData` (External): Global game data (e.g., gravity)

## Dependencies
- `Common/Thing.h`, `Common/ThingTemplate.h`, `Common/ThingFactory.h`
- `Common/GlobalData.h`, `Common/Player.h`, `GameLogic/TerrainLogic.h`
- `Lib/Trig.h` (for trigonometric functions)
- `Matrix3D`, `Coord3D`, `Vector3` (math types)
