# Generals/Code/Tools/WorldBuilder/include/BorderTool.h

## Purpose
Defines the BorderTool class for modifying map borders in WorldBuilder.

## Responsibilities
- Manages border modification operations (up, free, right)
- Handles mouse input for border editing
- Tracks border modification state
- Updates cursor during border editing

## Key Types
- **BorderTool (Class)**: Tool for editing map borders.
- **ModificationType (Enum)**: Border modification modes (invalid, up, free, right).

## Key Functions
### BorderTool()
- Purpose: Constructor.
- Calls: None.

### ~BorderTool()
- Purpose: Destructor.
- Calls: None.

### setCursor()
- Purpose: Sets the cursor for border editing.
- Calls: None.

### activate()
- Purpose: Activates the border tool.
- Calls: None.

### deactivate()
- Purpose: Deactivates the border tool.
- Calls: None.

### followsTerrain()
- Purpose: Returns whether the tool follows terrain.
- Calls: None.

### mouseMoved()
- Purpose: Handles mouse movement for border editing.
- Calls: None.

### mouseDown()
- Purpose: Handles mouse down for border editing.
- Calls: None.

### mouseUp()
- Purpose: Handles mouse up for border editing.
- Calls: None.

## Globals
- **m_mouseDown (Bool)**: Tracks mouse button
