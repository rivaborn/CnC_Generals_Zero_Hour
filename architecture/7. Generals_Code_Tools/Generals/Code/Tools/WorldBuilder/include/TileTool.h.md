# Generals/Code/Tools/WorldBuilder/include/TileTool.h

## Purpose
Defines base and derived classes for texture tiling tools in WorldBuilder.

## Responsibilities
- Provides abstract tile painting functionality
- Manages height map editing during texture application
- Handles mouse input for tile placement
- Supports tool activation/deactivation
- Allows width customization for larger tile tools

## Key Types
- **TileTool (Class)**: Base class for texture tiling tools.
- **BigTileTool (Class)**: Extended tile tool with adjustable width.
- **WorldHeightMapEdit (Class)**: Reference-counted height map editor (external).

## Key Functions
### TileTool::mouseDown
- Purpose: Handle mouse down event for tile placement.
- Calls: Not inferable.

### TileTool::mouseUp
- Purpose: Handle mouse up event for tile placement.
- Calls: Not inferable.

### TileTool::mouseMoved
- Purpose: Handle mouse movement during tile placement.
- Calls: Not inferable.

### TileTool::activate
- Purpose: Activate the tool and prepare for use.
- Calls: Not inferable.

### BigTileTool::activate
- Purpose: Activate the big tile tool with current width.
- Calls: Not inferable.

### BigTileTool::setWidth
- Purpose: Set the tile width for big tile operations.
- Calls: Not inferable.

## Globals
- **BigTileTool::m_currentWidth (Int)**: Static variable tracking current tile width.

## Dependencies
- `Tool.h` (base class)
- `WorldHeightMapEdit` (external class)
- `CPoint`, `WbView`, `CWorldBuilderDoc` (external types)
