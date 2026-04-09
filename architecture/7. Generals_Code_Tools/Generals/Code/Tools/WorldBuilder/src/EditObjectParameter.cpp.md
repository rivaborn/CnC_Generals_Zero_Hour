# Generals/Code/Tools/WorldBuilder/src/EditObjectParameter.cpp

## Purpose
Handles the UI dialog for selecting and setting object parameters in the WorldBuilder tool.

## Responsibilities
- Manages a tree view control for browsing available objects
- Populates the tree with objects from the ThingFactory
- Handles object selection and parameter assignment
- Provides hierarchical organization of objects by side and editor sorting

## Key Types
- **EditObjectParameter (class)**: Dialog class for object parameter editing
- **ThingTemplate (struct)**: Template data for game objects

## Key Functions
### EditObjectParameter::OnInitDialog
- Purpose: Initializes the dialog and populates the object tree view
- Calls: `m_objectTreeView.Create`, `addObject`, `addObjectLists`

### EditObjectParameter::addObject
- Purpose: Adds a single object template to the tree view hierarchy
- Calls: `findOrAdd`

### EditObjectParameter::addObjectLists
- Purpose: Adds predefined object lists to the tree view
- Calls: `EditParameter::loadObjectTypeList`, `findOrAdd`

### EditObjectParameter::findOrAdd
- Purpose: Finds or creates a tree view item with the given label
- Calls: `m_objectTreeView.GetChildItem`, `m_objectTreeView.GetItem`, `m_objectTreeView.InsertItem`

### EditObjectParameter::OnOK
- Purpose: Handles the OK button click, setting the selected object as the parameter value
- Calls: `m_objectTreeView.GetSelectedItem`, `m_objectTreeView.GetItem`, `m_parameter->friend_setString`

## Globals
- **TheThingFactory (ThingFactory**)**: Global factory for game object templates

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `EditObjectParameter.h`, `EditParameter.h`
- `GameLogic/Scripts.h`, `GameLogic/SidesList.h`, `GameLogic/PolygonTrigger.h`
- `Common/ThingTemplate.h`, `Common/ThingFactory.h`, `Common/ThingSort.h`
- MFC classes: `CDialog`, `CWnd`, `CRect`, `TVINSERTSTRUCT`, `TVITEM`
- Windows API: `MessageBeep`
