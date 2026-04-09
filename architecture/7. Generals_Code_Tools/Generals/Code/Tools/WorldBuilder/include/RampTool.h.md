# Generals/Code/Tools/WorldBuilder/include/RampTool.h

## Purpose
Defines the RampTool class for the WorldBuilder editor, used to create ramps in terrain.

## Responsibilities
- Manages ramp creation via mouse input
- Tracks start/end points and curve point for ramp shape
- Handles tool activation/deactivation
- Renders feedback during ramp creation
- Applies ramp modifications to the document

## Key Types
- **RampTool (Class)**: Tool for creating ramps in terrain editing.

## Key Functions
### RampTool()
- Purpose: Constructor for RampTool.
- Calls: None

### activate()
- Purpose: Activates the ramp tool.
- Calls: None

### deactivate()
- Purpose: Deactivates the ramp tool.
- Calls: None

### followsTerrain()
- Purpose: Indicates whether the tool follows terrain.
- Calls: None

### mouseMoved()
- Purpose: Handles mouse movement for ramp creation.
- Calls: drawFeedback()

### mouseDown()
- Purpose: Handles mouse down event for ramp start point.
- Calls: None

### mouseUp()
- Purpose: Handles mouse up event to finalize ramp.
- Calls: applyRamp()

### drawFeedback()
- Purpose: Renders visual feedback during ramp creation.
- Calls: None

### applyRamp()
- Purpose: Applies the ramp modification to the document.
- Calls: None

## Globals
- None

## Dependencies
- **Tool.h**: Base class for tools
- **Coord3D**: 3D coordinate type
- **CPoint**: Point type
- **WbView**: View class
- **CWorldBuilderDoc**: Document class for WorldBuilder
