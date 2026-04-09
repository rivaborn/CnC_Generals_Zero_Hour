# Generals/Code/Tools/WorldBuilder/include/ScorchTool.h

## Purpose
Defines the ScorchTool class, a tool for applying scorch effects in WorldBuilder.

## Responsibilities
- Handles mouse interactions for scorch effect placement
- Manages scorch object selection and placement
- Implements tool activation/deactivation lifecycle
- Tracks mouse down position for scorch operations

## Key Types
- ScorchTool (Class): Tool for applying scorch effects in the editor
- WorldHeightMapEdit (Class): Forward declaration for heightmap editing
- MapObject (Class): Forward declaration for map objects

## Key Functions
### ScorchTool::pickScorch
- Purpose: Selects a scorch object at the given location
- Calls: Not inferable

### ScorchTool::mouseDown
- Purpose: Handles mouse down event for scorch placement
- Calls: Not inferable

### ScorchTool::mouseMoved
- Purpose: Handles mouse movement during scorch placement
- Calls: Not inferable

### ScorchTool::mouseUp
- Purpose: Handles mouse up event to finalize scorch placement
- Calls: Not inferable

### ScorchTool::activate
- Purpose: Activates the scorch tool
- Calls: Not inferable

### ScorchTool::deactivate
- Purpose: Deactivates the scorch tool
- Calls: Not inferable

## Globals
- None

## Dependencies
- Tool.h (base class)
- Forward declarations: WorldHeightMapEdit, MapObject
- CPoint, WbView, CWorldBuilderDoc (external types)
- Coord3D (coordinate structure)
