# Generals/Code/Tools/WorldBuilder/src/BuildList.cpp

## Purpose
Manages the build list UI and functionality in WorldBuilder, allowing users to edit build orders for factions.

## Responsibilities
- Handles UI events for build list manipulation (add, delete, reorder)
- Manages build list properties (angle, height, rebuilds, initially built status)
- Exports build lists to INI files
- Updates energy consumption/production calculations
- Synchronizes build list state with the document

## Key Types
- **BuildList (class)**: Main dialog class for build list management
- **BuildListInfo (external)**: Represents individual build list entries
- **SidesInfo (external)**: Contains faction-specific build lists
- **SidesList (external)**: Manages all factions and their build lists

## Key Functions
### OnInitDialog
- Purpose: Initializes the dialog and loads initial data
- Calls: loadSides, updateCurSide

### updateCurSide
- Purpose: Refreshes the build list display for the current faction
- Calls: TheSidesList->getSideInfo, pSide->getBuildList

### addBuilding
- Purpose: Adds a new building to the current faction's build list
- Calls: newInstance, pSide->addToBuildList, pDoc->AddAndDoUndoable

### OnSelchangeBuildList
- Purpose: Updates UI controls when a build list entry is selected
- Calls: pSide->getBuildList, TheThingFactory->findTemplate

### OnExport
- Purpose: Exports the current build list to an INI file
- Calls: fopen, fprintf, ThePlayerTemplateStore->findPlayerTemplate

## Globals
- **m_staticThis (BuildList*)**: Static pointer to the dialog instance
- **m_updating (Bool)**: Flag to prevent recursive updates

## Dependencies
- MFC dialog framework (CDialog, CListBox, CComboBox)
- WorldBuilder document classes (CWorldBuilderDoc, WbView3d)
- Game logic classes (SidesList, SidesInfo, BuildListInfo)
- Common utilities (ThingFactory, ThingTemplate)
- Undo system (SidesListUndoable, CUndoable)
