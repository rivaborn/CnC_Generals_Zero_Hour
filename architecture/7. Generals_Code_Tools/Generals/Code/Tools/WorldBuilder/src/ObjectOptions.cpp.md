# Generals/Code/Tools/WorldBuilder/src/ObjectOptions.cpp

## Purpose
Handles the object selection and configuration UI in the WorldBuilder tool, managing map objects and their properties.

## Responsibilities
- Manages the object selection tree view
- Handles object ownership/team assignment
- Provides object preview functionality
- Supports object duplication and placement
- Maintains object list and selection state

## Key Types
- `ObjectOptions` (Class): Main dialog class for object options
- `MapObject` (Class): Represents objects in the map
- `ThingTemplate` (Class): Template data for objects
- `EditorSortingType` (Enum): Categories for organizing objects

## Key Functions
### `findSideListEntryWithPlayerOfSide`
- Purpose: Finds a side entry matching a player side
- Calls: `TheSidesList->getNumSides()`, `TheSidesList->getSideInfo()`, `ThePlayerTemplateStore->findPlayerTemplate()`

### `updateLabel`
- Purpose: Updates the UI to reflect current object selection
- Calls: `getCurMapObject()`, `findSideListEntryWithPlayerOfSide()`, `TheSidesList->getNumTeams()`, `TheSidesList->getTeamInfo()`

### `duplicateCurMapObjectForPlace`
- Purpose: Creates a copy of the currently selected object for placement
- Calls: `getCurMapObject()`, `AddPlayerDialog::DoModal()`, `TheSidesList->getNumSides()`, `TheSidesList->getSideInfo()`

### `addObject`
- Purpose: Adds an object to the tree view hierarchy
- Calls: `findOrAdd()`, `ThingTemplate->getEditorSorting()`

## Globals
- `m_staticThis` (ObjectOptions*): Singleton instance pointer
- `m_updating` (Bool): Flag for UI update state
- `m_currentObjectName` (char[]): Name of currently selected object
- `m_currentObjectIndex` (Int): Index of currently selected object
- `m_curOwnerName` (AsciiString): Current owner team name

## Dependencies
- `stdafx.h`, `resource.h`, `Lib\BaseType.h`, `ObjectOptions.h`
- `WHeightMapEdit.h`, `AddPlayerDialog.h`, `WorldBuilderDoc.h`
- `CUndoable.h`, `W3DDevice/GameClient/HeightMap.h`
- `Common/WellKnownKeys.h`, `Common/ThingTemplate.h`
- `Common/ThingFactory.h`, `Common/ThingSort.h`
- `Common/PlayerTemplate.h`, `Common/FileSystem.h`
- `GameLogic/SidesList.h`, `GameClient/Color.h`
- `<list>`
