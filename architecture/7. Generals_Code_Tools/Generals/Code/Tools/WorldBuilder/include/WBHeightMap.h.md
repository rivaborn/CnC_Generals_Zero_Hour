# Generals/Code/Tools/WorldBuilder/include/WBHeightMap.h

## Purpose
Defines the WBHeightMap class, a specialized height map renderer for the WorldBuilder tool.

## Responsibilities
- Render height maps in the WorldBuilder editor
- Handle ray casting for height map interactions
- Provide height query methods for terrain editing
- Manage flattening and drawing modes for the height map

## Key Types
- WBHeightMap (Class): Specialized height map renderer for WorldBuilder

## Key Functions
### WBHeightMap()
- Purpose: Default constructor for WBHeightMap.
- Calls: None

### Render()
- Purpose: Renders the height map.
- Calls: None (implementation not shown)

### Cast_Ray()
- Purpose: Performs ray casting against the height map.
- Calls: None (implementation not shown)

### getHeightMapHeight()
- Purpose: Returns height and normal at a given point.
- Calls: None (implementation not shown)

### getMaxCellHeight()
- Purpose: Returns maximum height of the 4 cell corners.
- Calls: None (implementation not shown)

### setFlattenHeights()
- Purpose: Sets the flatten heights mode.
- Calls: flattenHeights()

### flattenHeights()
- Purpose: Flattens the height map.
- Calls: None (implementation not shown)

## Globals
- None

## Dependencies
- HeightMapRenderObjClass (base class)
- RenderInfoClass (used in Render)
- RayCollisionTestClass (used in Cast_Ray)
- Coord3D (used in getHeightMapHeight)
