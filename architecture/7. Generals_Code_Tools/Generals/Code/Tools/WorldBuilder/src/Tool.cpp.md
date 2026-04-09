# Generals/Code/Tools/WorldBuilder/src/Tool.cpp

## Purpose
Base class for texture tiling tools in WorldBuilder, providing core functionality for brush operations.

## Responsibilities
- Manages tool cursor and activation
- Calculates blend factors for brush operations
- Converts document coordinates to cell indices
- Retrieves cell indices within a rectangular area

## Key Types
- **Tool (Class)**: Base class for WorldBuilder tools
- **Coord3D (Type)**: 3D coordinate structure
- **CPoint (Type)**: 2D point structure
- **VecHeightMapIndexes (Type)**: Collection of height map indices

## Key Functions
### Tool::Tool(Int toolID, Int cursorID)
- Purpose: Constructor initializes tool with ID and cursor ID
- Calls: None

### Tool::activate()
- Purpose: Shows the "no options" dialog and disables brush feedback
- Calls: CMainFrame::GetMainFrame()->showOptionsDialog, DrawObject::setDoBrushFeedback

### Tool::calcRoundBlendFactor(CPoint center, Int x, Int y, Int brushWidth, Int featherWidth)
- Purpose: Calculates blend factor for round brush
- Calls: None

### Tool::calcSquareBlendFactor(CPoint center, Int x, Int y, Int brushWidth, Int featherWidth)
- Purpose: Calculates blend factor for square brush
- Calls: None

### Tool::getCenterIndex(Coord3D *docLocP, Int brushWidth, CPoint *center, CWorldBuilderDoc *pDoc)
- Purpose: Converts document coordinates to cell index for brush center
- Calls: CWorldBuilderDoc::getCellIndexFromCoord

### Tool::getAllIndexesIn(const Coord3D *bl, const Coord3D *br, const Coord3D *tl, const Coord3D *tr, Int
