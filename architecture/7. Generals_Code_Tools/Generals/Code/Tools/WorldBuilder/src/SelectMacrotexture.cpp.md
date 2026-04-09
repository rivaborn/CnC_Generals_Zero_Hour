# Generals/Code/Tools/WorldBuilder/src/SelectMacrotexture.cpp

## Purpose
Handles the UI dialog for selecting macrotextures in WorldBuilder, populating a tree view with available TGA files and applying the selected texture to the terrain.

## Responsibilities
- Creates and manages a tree view control for texture selection
- Scans the Art/TestModelsHere directory for TGA files
- Updates the terrain's macrotexture when a selection is made
- Provides a default option to clear the macrotexture

## Key Types
- SelectMacrotexture (Class): Dialog class for macrotexture selection
- CTreeView (Member): Tree control displaying available textures

## Key Functions
### OnInitDialog
- Purpose: Initializes the dialog and populates the tree view with TGA files
- Calls: TheFileSystem->getFileListInDirectory, m_textureTreeView.InsertItem

### OnNotify
- Purpose: Handles tree view selection changes and updates the terrain's macrotexture
- Calls: TheTerrainRenderObject->updateMacroTexture, TheWritableGlobalData->m_useLightMap assignment

## Globals
- DEFAULT (const char*): String literal for the default texture option

## Dependencies
- stdafx.h, worldbuilder.h, SelectMacrotexture.h
- Common/FileSystem.h, common/GlobalData.h, W3DDevice/GameClient/HeightMap.h
- MFC classes (CDialog, CTreeView, etc.)
- TheFileSystem, TheTerrainRenderObject, TheWritableGlobalData (global instances)
