# Generals/Code/Tools/WorldBuilder/src/WaterTool.cpp

## Purpose
Implements the water area tool for the WorldBuilder editor, allowing creation and modification of water polygons.

## Responsibilities
- Handles water polygon creation, selection, and editing
- Manages water height and area filling logic
- Provides undo/redo functionality for water edits
- Controls tool activation/deactivation and cursor behavior

## Key Types
- **WaterTool (Class)**: Main tool class for water editing
- **PolygonTrigger (Class)**: Represents water polygons
- **WaterOptions (Class)**: Stores water tool settings

## Key Functions
### mapZtoHeight
- Purpose: Converts map Z coordinate to height value
- Calls: None

### fillTheArea
- Purpose: Fills an area with water based on mouse position
- Calls: getCenterIndex, mapZtoHeight, adjustSpacing, AddPolygonUndoable

### adjustSpacing
- Purpose: Adjusts polygon point spacing for better water area representation
- Calls: None

## Globals
- **m_water_isActive (Bool)**: Tracks if water tool is active
- **doIt (Bool)**: Internal flag for tool operation

## Dependencies
- "StdAfx.h", "resource.h", "WaterTool.h", "CUndoable.h", "PointerTool.h", "TerrainMaterial.h", "WHeightMapEdit.h", "WorldBuilderDoc.h", "WorldBuilderView.h", "MainFrm.h", "DrawObject.h", "GameLogic/PolygonTrigger.h", "Common/GlobalData.h"
