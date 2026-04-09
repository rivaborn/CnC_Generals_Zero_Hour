# Generals/Code/Tools/WorldBuilder/include/FloodFillTool.h

## Purpose
Defines the FloodFillTool class for texture tiling in WorldBuilder, allowing users to fill areas with a selected texture.

## Responsibilities
- Implements texture filling functionality for WorldBuilder.
- Manages texture selection and cliff adjustment settings.
- Handles mouse interactions for texture application.
- Sets appropriate cursor for the tool.
- Provides activation/deactivation logic for the tool.

## Key Types
- **FloodFillTool (Class)**: Texture filling tool for WorldBuilder.
- **WorldHeightMapEdit (Class)**: External class for heightmap editing (forward declared).

## Key Functions
### FloodFillTool::mouseUp
- Purpose: Handles mouse release event for texture filling.
- Calls: Not inferable (implementation in .cpp).

### FloodFillTool::activate
- Purpose: Activates the tool, making it the current selection.
- Calls: Not inferable.

### FloodFillTool::setCursor
- Purpose: Sets the cursor appropriate for this tool.
- Calls: Not inferable.

### FloodFillTool::getAdjustCliffs
- Purpose: Returns whether cliff textures should be adjusted.
- Calls: None.

### FloodFillTool::setAdjustCliffs
- Purpose: Sets whether cliff textures should be adjusted.
- Calls: None.

## Globals
- **m_adjustCliffTextures (Bool, static)**: Controls whether cliff textures are adjusted during filling.

## Dependencies
- **Tool.h**: Base class for WorldBuilder tools.
- **WbView**: View class for WorldBuilder (used in parameters).
- **CWorldBuilderDoc**: Document class for WorldBuilder (used in parameters).
- **CPoint**: Point structure (likely from MFC).
- **HCURSOR**: Windows cursor handle type.
