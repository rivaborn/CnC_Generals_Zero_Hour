# Generals/Code/Tools/WorldBuilder/src/BlendMaterial.cpp

## Purpose
Handles the BlendMaterial dialog in WorldBuilder, managing terrain texture blending selection.

## Responsibilities
- Manages UI for selecting blend textures in a tree view
- Updates terrain texture list dynamically
- Handles tree view selection changes and updates document state
- Maintains current blend texture state

## Key Types
- BlendMaterial (Class): Dialog class for terrain blending UI
- None: No other classes/structs/enums defined

## Key Functions
### BlendMaterial::setBlendTexClass
- Purpose: Sets the current blend texture and updates UI selection
- Calls: setTerrainTreeViewSelection

### BlendMaterial::setTerrainTreeViewSelection
- Purpose: Recursively selects a texture in the tree view by its index
- Calls: m_terrainTreeView.GetChildItem, m_terrainTreeView.GetItem, m_terrainTreeView.SelectItem

### BlendMaterial::OnInitDialog
- Purpose: Initializes the dialog controls and tree view
- Calls: CDialog::OnInitDialog, m_terrainTreeView.Create, updateTextures

### BlendMaterial::addTerrain
- Purpose: Adds a terrain entry to the tree view if it's a blend edge
- Calls: TheTerrainTypes->findTerrain, findOrAdd, m_terrainTreeView.InsertItem

### BlendMaterial::updateTextures
- Purpose: Rebuilds the entire texture tree view from current texture classes
- Calls: m_terrainTreeView.DeleteAllItems, addTerrain, setTerrainTreeViewSelection

### BlendMaterial::OnNotify
- Purpose: Handles tree view selection changes and updates document
- Calls: CWorldBuilderDoc::GetActiveDoc, GetHeightMap

## Globals
- m_staticThis (BlendMaterial*): Static pointer to the dialog instance
- defaultMaterialIndex (Int): Default selected material index (-1)

## Dependencies
- "stdafx.h", "resource.h", "Lib\BaseType.h", "BlendMaterial.h", "WHeightMapEdit.h", "WorldBuilderDoc.h", "TileTool.h", "Common/TerrainTypes.h", "W3DDevice/GameClient/TerrainTex.h"
- COptionsPanel, CDialog, CWnd, CRect, CString, TVITEM, TVINSERTSTRUCT, NMTREEVIEW, HTREEITEM, AsciiString, WorldHeightMapEdit, CWorldBuilderDoc, TheTerrainTypes, TerrainType
