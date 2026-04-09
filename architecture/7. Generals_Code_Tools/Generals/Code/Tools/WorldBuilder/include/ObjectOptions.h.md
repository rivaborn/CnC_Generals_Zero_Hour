# Generals/Code/Tools/WorldBuilder/include/ObjectOptions.h

## Purpose
Header file for the `ObjectOptions` dialog class used in WorldBuilder for managing map objects.

## Responsibilities
- Manages object selection and properties in WorldBuilder
- Provides UI for object manipulation (tree view, preview)
- Handles object ownership and team assignment
- Supports object duplication and placement
- Maintains current object state and selection

## Key Types
- **ObjectOptions (Class)**: Dialog for object management in WorldBuilder
- **MapObject (Class)**: Represents a map object (forward declared)
- **WorldHeightMapEdit (Class)**: Height map editor (forward declared)
- **(anonymous enum)**: Contains `NAME_MAX_LEN = 64`
- **(anonymous enum)**: Contains `IDD = IDD_OBJECT_OPTIONS`

## Key Functions
### `addObject`
- Purpose: Adds an object to the tree view under a specified parent.
- Calls: None visible in header.

### `findOrAdd`
- Purpose: Finds or adds a tree view item with the given label.
- Calls: None visible in header.

### `findOrDont`
- Purpose: Finds a tree view item without adding it.
- Calls: None visible in header.

### `duplicateCurMapObjectForPlace`
- Purpose: Duplicates the currently selected object for placement.
- Calls: None visible in header.

### `update`
- Purpose: Updates the dialog's state and UI.
- Calls: None visible in header.

## Globals
- **m_staticThis (ObjectOptions*)**: Static pointer to the dialog instance.
- **m_updating (Bool)**: Flag indicating if the dialog is updating.
- **m_currentObjectIndex (Int)**: Index of the currently selected object.
- **m_currentObjectName (char[NAME_MAX_LEN])**: Name of the currently selected object.
- **m_curOwner
