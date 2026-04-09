# Generals/Code/Tools/WorldBuilder/src/PickUnitDialog.cpp

## Purpose
Implements dialog classes for selecting units in the WorldBuilder editor.

## Responsibilities
- Manages unit selection UI via tree view
- Filters units by type and faction
- Handles dialog initialization and message routing
- Provides access to selected unit data

## Key Types
- **PickUnitDialog (class)**: Main dialog for unit selection
- **ReplaceUnitDialog (class)**: Specialized dialog for replacing units
- **MapObject (struct)**: Represents objects in the tree view
- **EditorSortingType (enum)**: Categories for sorting units

## Key Functions
### `OnInitDialog`
- Purpose: Initializes the dialog and populates the tree view with units
- Calls: `TheThingFactory->firstTemplate()`, `newInstance(MapObject)`, `addObject`

### `addObject`
- Purpose: Adds an object to the tree view with proper hierarchy
- Calls: `findOrAdd`, `m_objectTreeView.InsertItem`

### `getPickedThing`
- Purpose: Returns the selected unit's template
- Calls: `TheThingFactory->firstTemplate()`

## Globals
- **TheThingFactory (ThingFactory**)**: Global factory for game objects

## Dependencies
- `ThingTemplate.h`, `WHeightMapEdit.h`, `WorldBuilderDoc.h`
- MFC classes (`CDialog`, `CWnd`, etc.)
- `ThingFactory`, `ThingSort` headers
