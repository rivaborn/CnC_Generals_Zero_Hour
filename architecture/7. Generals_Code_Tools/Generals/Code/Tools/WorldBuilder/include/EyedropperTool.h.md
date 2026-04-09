# Generals/Code/Tools/WorldBuilder/include/EyedropperTool.h

## Purpose
Defines the EyedropperTool class for selecting textures in WorldBuilder.

## Responsibilities
- Implements texture selection functionality
- Handles mouse input for texture picking
- Integrates with WorldBuilder's tool system
- Provides activation/deactivation behavior

## Key Types
- EyedropperTool (Class): Texture selection tool for WorldBuilder
- WorldHeightMapEdit (Class): External dependency for heightmap editing

## Key Functions
### EyedropperTool()
- Purpose: Constructor for EyedropperTool
- Calls: None

### ~EyedropperTool()
- Purpose: Destructor for EyedropperTool
- Calls: None

### mouseDown()
- Purpose: Handles mouse down event for texture selection
- Calls: None (implementation not shown)

### activate()
- Purpose: Activates the eyedropper tool
- Calls: None (implementation not shown)

## Globals
None

## Dependencies
- Tool.h (base class)
- WorldHeightMapEdit (forward declaration)
- TTrackingMode, CPoint, WbView, CWorldBuilderDoc (external types)
