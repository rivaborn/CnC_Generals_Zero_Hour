# Generals/Code/Tools/WorldBuilder/include/RoadTool.h

## Purpose
Defines the `RoadTool` class for adding road segments in WorldBuilder.

## Responsibilities
- Manages road segment creation via mouse input
- Handles snapping roads to existing segments
- Tracks road placement state (hysteresis, minimum length)
- Integrates with WorldBuilder's tool system

## Key Types
- **RoadTool (Class)**: Road segment placement tool.
- **WorldHeightMapEdit (Class)**: External heightmap editing interface.
- **(anonymous enum) (Enum)**: Contains `HYSTERESIS` and `MIN_LENGTH` constants.

## Key Functions
### `findSegment`
- Purpose: Locates the nearest road segment to a given point.
- Calls: Not inferable.

### `snap`
- Purpose: Snaps a coordinate to the nearest road segment.
- Calls: Not inferable.

### `mouseDown`
- Purpose: Initiates road placement on mouse down.
- Calls: Not inferable.

### `mouseMoved`
- Purpose: Updates road placement during mouse movement.
- Calls: Not inferable.

### `mouseUp`
- Purpose: Finalizes road placement on mouse release.
- Calls: Not inferable.

### `activate`
- Purpose: Activates the road tool.
- Calls: Not inferable.

## Globals
- **ROAD_SNAP_DISTANCE (float)**: Maximum distance for road snapping (1.0f).

## Dependencies
- `Tool.h` (base class)
- `W3DDevice/GameClient/WorldHeightMap.h` (heightmap access)
- `MapObject` (game object reference)
- `Coord3D` (3D coordinate type)
- `TTrackingMode`, `CPoint`, `WbView`, `CWorldBuilderDoc` (WorldBuilder UI types)
