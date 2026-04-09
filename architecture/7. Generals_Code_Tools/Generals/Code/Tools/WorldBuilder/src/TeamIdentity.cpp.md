# Generals/Code/Tools/WorldBuilder/src/TeamIdentity.cpp

## Purpose
Handles the UI and logic for editing team properties in the WorldBuilder tool.

## Responsibilities
- Manages team identity property page UI
- Loads and saves team configuration data
- Handles unit type selection and validation
- Manages team ownership and singleton settings
- Processes user input for team parameters

## Key Types
- TeamIdentity (Class): Property page for team editing
- None

## Key Functions
### OnInitDialog
- Purpose: Initializes the dialog with team data
- Calls: loadUnitsInfo, EditParameter::loadWaypoints, TheSidesList->getNumSides, TheSidesList->findSideInfo

### loadUnitsInfo
- Purpose: Loads unit type information for a specific unit slot
- Calls: TheThingFactory->firstTemplate, tTemplate->friend_getNextTemplate

### OnCommand
- Purpose: Handles command notifications from controls
- Calls: None directly visible

### OnUnitTypeButton
- Purpose: Opens unit selection dialog for a specific unit slot
- Calls: PickUnitDialog constructor, dlg.DoModal

### OnKillfocusTeamName
- Purpose: Validates and updates team name when focus is lost
- Calls: m_sides->findTeamInfo, m_sides->findSideInfo, MapObject::countMapObjectsWithOwner

## Globals
- NEUTRAL_NAME_STR (const char*): String for neutral team name

## Dependencies
- stdafx.h, worldbuilder.h, TeamIdentity.h, EditParameter.h, PickUnitDialog.h
- Common/WellKnownKeys.h, Common/ThingTemplate.h, Common/ThingFactory.h
- Common/ThingSort.h, GameLogic/SidesList.h
- MFC classes (CPropertyPage, CDataExchange, CComboBox, CEdit, CButton, CWnd)
- AsciiString, NameKeyType, Bool, Int, EditorSortingType, ThingTemplate, SidesList
