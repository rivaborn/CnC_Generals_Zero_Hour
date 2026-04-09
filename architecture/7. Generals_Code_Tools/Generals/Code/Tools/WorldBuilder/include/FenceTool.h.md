# Generals/Code/Tools/WorldBuilder/include/FenceTool.h

## Purpose
Defines the `FenceTool` class for texture tiling operations in WorldBuilder.

## Responsibilities
- Handles mouse input for fence tool operations
- Manages map object placement and updates
- Tracks tool state during activation/deactivation
- Calculates object positioning based on mouse movement

## Key Types
- **FenceTool (Class)**: Main tool class for fence operations
- **WorldHeightMapEdit (Class)**: External dependency for heightmap edits
- **MapObject (Class)**: External dependency for map objects
- **Vector3 (Class)**: External dependency for 3D coordinates

## Key Functions
### FenceTool::updateMapObjectList
- Purpose: Updates the list of map objects based on mouse positions
- Calls: Not inferable

### FenceTool::mouseDown
- Purpose: Handles mouse down event for fence tool
- Calls: Not inferable

### FenceTool::mouseUp
- Purpose: Handles mouse up event for fence tool
- Calls: Not inferable

### FenceTool::mouseMoved
- Purpose: Handles mouse movement for fence tool
- Calls: Not inferable

### FenceTool::activate
- Purpose: Activates the fence tool
- Calls: Not inferable

### FenceTool::deactivate
- Purpose: Deactivates the fence tool
- Calls: Not inferable

## Globals
- **m_downPt2d (CPoint)**: Stores the 2D mouse down position
- **m_downPt3d (Coord3D)**: Stores the 3D mouse down position
- **m_mapObjectList (MapObject*)**: Pointer to list of map objects
- **m_curObjectWidth (Real)**: Current object width
- **m_curObjectOffset (Real)**: Current object offset
- **m
