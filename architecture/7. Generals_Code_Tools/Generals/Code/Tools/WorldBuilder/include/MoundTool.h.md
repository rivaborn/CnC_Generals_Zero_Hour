# Generals/Code/Tools/WorldBuilder/include/MoundTool.h

## Purpose
Defines tools for modifying terrain height in WorldBuilder, including mounding and digging functionality.

## Responsibilities
- Manage terrain height modifications via brush tools
- Handle mouse input for terrain editing
- Maintain tool state and parameters (height, width, feather)
- Provide access to height map data

## Key Types
- **MoundTool (Class)**: Base class for terrain height editing tools
- **DigTool (Class)**: Derived class for digging functionality
- **(anonymous enum) (Enum)**: Contains MIN_DELAY_TIME constant
- **MIN_DELAY_TIME (Enum)**: Minimum delay between tool applications (60ms)

## Key Functions
### MoundTool::mouseDown
- Purpose: Handle mouse down event for terrain editing
- Calls: Not inferable

### MoundTool::mouseUp
- Purpose: Handle mouse up event for terrain editing
- Calls: Not inferable

### MoundTool::mouseMoved
- Purpose: Handle mouse movement for terrain editing
- Calls: Not inferable

### MoundTool::activate
- Purpose: Activate the tool as the current tool
- Calls: Not inferable

## Globals
- **m_moundHeight (Int)**: Static variable for mound height setting
- **m_brushWidth (Int)**: Static variable for brush width setting
- **m_brushFeather (Int)**: Static variable for brush feather setting

## Dependencies
- **Tool.h**: Base class for tools
- **WorldHeightMapEdit**: Class for height map editing (forward declared)
- **TTrackingMode, CPoint, WbView, CWorldBuilderDoc**: UI and document classes
