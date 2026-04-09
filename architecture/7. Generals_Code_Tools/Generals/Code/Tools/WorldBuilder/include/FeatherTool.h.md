# Generals/Code/Tools/WorldBuilder/include/FeatherTool.h

## Purpose
Defines the FeatherTool class for smooth height map editing in WorldBuilder.

## Responsibilities
- Smooths height map edits using feathering
- Manages mouse input for terrain modification
- Maintains height map edit copies for undo/redo
- Provides tool activation/deactivation

## Key Types
- FeatherTool (Class): Smooth height map editing tool
- WorldHeightMapEdit (Class): Reference to height map data (external)

## Key Functions
### FeatherTool()
- Purpose: Constructor for FeatherTool
- Calls: None

### ~FeatherTool()
- Purpose: Destructor for FeatherTool
- Calls: None

### setFeather()
- Purpose: Sets the feathering amount
- Calls: None

### setRate()
- Purpose: Sets the rate parameter
- Calls: None

### setRadius()
- Purpose: Sets the radius parameter
- Calls: None

### mouseDown()
- Purpose: Handles mouse down events for terrain editing
- Calls: None (implementation in .cpp)

### mouseUp()
- Purpose: Handles mouse up events for terrain editing
- Calls: None (implementation in .cpp)

### mouseMoved()
- Purpose: Handles mouse movement for terrain editing
- Calls: None (implementation in .cpp)

### getHeightMap()
- Purpose: Returns the current height map edit copy
- Calls: None

### activate()
- Purpose: Activates the tool
- Calls: None (implementation in .cpp)

## Globals
- m_feather (Int): Static feathering amount
- m_rate (Int): Static rate parameter
- m_radius (Int): Static radius parameter

## Dependencies
- Tool.h (base class)
- WorldHeightMapEdit (forward declaration)
- TTrackingMode, CPoint, W
